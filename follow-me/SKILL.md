---
name: follow-me
description: >
  Activates FOLLOW-ME — a sequential workflow executor that follows a numbered markdown task list
  step by step, never skipping, never forgetting, maintaining full context across all steps.
  Trigger when the user says "usa follow-me", "activa follow-me", "sigue estos pasos", "ejecuta
  este workflow", "sigue esta lista", "ejecuta paso a paso", or when the user provides a numbered
  markdown list and wants each step executed in strict order. Also trigger when the user pastes
  a task list with `1.`, `2.`, `3.` items and says things like "haz esto", "sigue esto",
  "ejecuta esto", "follow these steps", or "do this step by step". ALWAYS use this skill over
  generic step-by-step reasoning whenever a numbered markdown list is the primary input and
  sequential execution is required.
---

# FOLLOW-ME — Sequential Workflow Executor

## ATOM

$$\text{CoT} := s_0 \xrightarrow{\phi_{\text{md}}(\ell)} \mathcal{W} \xrightarrow{n_1,\Gamma_1} \cdots \xrightarrow{n_{|N|},\Gamma_{|N|}} s_{\text{done}}$$

---

## [PHASE 0 — PARSE]

On activation, immediately parse the user's input as a markdown numbered list.

**Grammar:**
```
N. <operation> [cond: <predicate>] [retry: <n>] [parallel: <group>]
```

**Rules:**
- Match lines with regex `^\d+\.\s+(.+)$`
- Extract `id` (number) and `op` (description) for each step
- Build sequential edges: `n_i → n_{i+1}` for all `i`
- Default edge condition: `π = true` (unconditional)
- Inline annotations `[cond:]`, `[retry:]`, `[parallel:]` override defaults
- If ANY line fails to match → halt and ask user to fix the list before proceeding

**Output of PARSE:** Internal step registry `N = {n_1, n_2, ..., n_k}`, ordered.

---

## [PHASE 1 — ANNOUNCE]

Before executing, display the full parsed plan to the user:

```
📋 WORKFLOW LOADED — N steps detected

  ✦ Step 1: <op_1>
  ✦ Step 2: <op_2>
  ...
  ✦ Step N: <op_N>

▶ Starting execution...
```

This makes the full scope visible and signals the agent is tracking all steps.

---

## [PHASE 2 — EXECUTE]

### Core invariants (NEVER violate)

| Invariant | Rule |
|---|---|
| **Strict order** | `exec(n_{i+1})` only if `n_i ∈ R` |
| **Gate** | `n_{i+1}` is blocked until `n_i` completes |
| **Amnesia prevention** | Context `Γ` is append-only — never reset mid-workflow |
| **Completeness** | `DONE ⟺ R = N` — every step must enter `R` |

### Per-step execution protocol

For each `n_i` in order `1 → N`:

1. **HEADER** — Print before starting:
   ```
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━
   ▶ Step i/N — <op_i>
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━
   ```

2. **GATE CHECK** — Verify `n_{i-1} ∈ R`. If not → `s_wait` → error (should never happen in normal flow).

3. **EXECUTE** — Perform the operation `λ(n_i)` using all context `Γ_{i-1}`.

4. **OUTPUT** — Show result clearly. If the step produces an artifact (code, text, file), display it in full.

5. **REGISTER** — Append to progress register: `R ← R ∪ {n_i}`.

6. **CONTEXT UPDATE** — `Γ_i = Γ_{i-1} ∪ out(n_i)` — capture all outputs into context.

7. **TRACE** — Append `(n_i, t_i, out_i)` to trace `T`.

8. **FOOTER** — Print after completing:
   ```
   ✔ Step i complete  [R = i/N]
   ```

9. **PROCEED** — Move to `n_{i+1}` without waiting for user input (unless a `[cond:]` annotation requires it).

### Error handling

- If `λ(n_i)` fails and `[retry: θ]` is annotated → retry up to `θ` times before entering `s_err`
- On `s_err`: report failure, show `Γ_{i-1}` snapshot, halt and ask user how to proceed
- **Never silently skip a failed step**

### Interruption / resume

If the workflow is interrupted (user intervenes, crash, context lost):
- Restore from trace `T`: identify last `n_j ∈ R`
- Resume from `n_{j+1}` with `Γ_{j}` reconstructed from `T`
- Print: `↩ Resuming from step j+1/N`

---

## [PHASE 3 — COMPLETION]

When `R = N`:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ WORKFLOW COMPLETE
━━━━━━━━━━━━━━━━━━━━━━━━━━━

All N steps executed. No step was skipped.

Summary:
  ✔ Step 1: <op_1> → <one-line outcome>
  ✔ Step 2: <op_2> → <one-line outcome>
  ...
  ✔ Step N: <op_N> → <one-line outcome>
```

---

## [BOUNDARY CONSTRAINTS]

- **Never** ask the user for permission to move to the next step (unless a `[cond:]` requires external input)
- **Never** summarize a step without executing it
- **Never** merge two steps into one — respect the user's granularity
- **Never** reorder steps — the user's numbering is canonical
- **Always** show which step you are on (`i/N`) so the user can track progress
- **Always** carry forward all outputs from prior steps — later steps may depend on them

---

## [FORMAL INVARIANT SUMMARY]

$$\text{DONE} \iff R = N \iff |T| = |N| \iff \Gamma_{|N|} \supset \bigoplus_{i=1}^{|N|} \text{out}(n_i) \quad \blacksquare$$
