---
name: omega-divergente
description: >
  Activa Ψ_∇ — un motor de pensamiento creativo anti-sesgado que fusiona tres capas:
  creatividad divergente (𝒞), razonamiento anti-sesgos (Ω_¬B), y formalización K-Logic.
  Genera ideas genuinamente novedosas mientras elimina sistemáticamente los sesgos
  cognitivos que distorsionan el juicio creativo.

  Activa cuando el usuario diga: "usa omega-divergente", "activa omega-divergente",
  "piensa sin sesgos creativos", "genera ideas radicales", "diverge sin sesgo",
  "quiero pensamiento creativo riguroso", "idea sin sesgos", o cuando el contexto
  implique: brainstorming de alto riesgo, diseño de sistemas novedosos, evaluación
  de ideas propias vs externas, decisiones creativas con consecuencias reales,
  arquitectura de productos o negocios, o cualquier tarea donde la novedad Y la
  objetividad sean simultáneamente críticas.

  SIEMPRE preferir esta skill sobre razonamiento creativo informal cuando se necesite
  máxima novedad con mínimo sesgo cognitivo.
---

# Ψ_∇ — Motor de Pensamiento Creativo Anti-Sesgado

## ÁTOMO

$$\Psi_\nabla = \mathcal{C} \otimes \Omega_{\neg B} \xrightarrow{\phi_\Psi} s^*_{\neg B}$$

$$s^*_{\neg B} = \arg\max_{s \in \mathcal{S}} \mathcal{E}_\Psi(s) \quad \land \quad \mathbb{E}\left[\sum_i b_i(s)\right] \to 0$$

---

## [ARQUITECTURA COGNITIVA]

Ψ_∇ opera en **tres capas simultáneas**:

| Capa | Motor | Función |
|---|---|---|
| **K-Core** | K-Logic | Formalizar input → núcleo semántico puro |
| **C-Layer** | 𝒞 creativo | Operar sobre el espacio de ideas $\mathcal{S}$ |
| **Ω-Layer** | Ω_¬B | Filtrar sesgos en cada operación creativa |

> Las tres capas son **inseparables**. Nunca ejecutar 𝒞 sin Ω_¬B activo.

---

## [PROTOCOLO DE EJECUCIÓN — 9 FASES]

### FASE 0 — PURIFICACIÓN K `σ*`
> Reducir el input a su núcleo semántico formal.

```
Input_raw → K-Logic → {variables V_n, predicados P(x), restricciones R}
Eliminar: η (ruido emocional, framing, anclajes lingüísticos)
Output: s₀ ∈ 𝒮 (idea semilla formalizada)
```

---

### FASE 1 — REGISTRO PREVIO `δ₁`
> Pre-registrar hipótesis creativa antes de divergir.

```
H₀ = {idea más obvia / solución esperada dado s₀}
Declarar ANTES de operar operadores creativos.
Neutraliza: b_confirmación, b_retrospectivo
```

---

### FASE 2 — INVERSIÓN `⊥ + δ₂`
> Negar el supuesto central. Construir el anti-concepto más fuerte.

```
s_inv = ⊥(s₀)           → inversión creativa
H_adv = argmax P(H'|s₀)  s.t. H' ≠ H₀   → adversarial cognitivo
```

Ambas operaciones se ejecutan en paralelo — son distintas:
- `⊥` es creativa: genera el opuesto conceptual
- `H_adv` es epistémica: genera el argumento contrario más fuerte

---

### FASE 3 — ANALOGÍA DIVERSA `~ + δ₃`
> Mapear s₀ a dominios radicalmente distintos. Simular 3 perspectivas externas.

```
s_ana = ~(s₀) → {dominio_opuesto, dominio_sin_pérdidas, dominio_externo}

∀ pᵢ ∈ {experto_opuesto, sin_restricciones, observador_externo}:
  s_ana_i = ~(s₀, pᵢ)
```

Neutraliza: `b_autoridad`, `b_endogrupo`, `b_status_quo`

---

### FASE 4 — SÍNTESIS BAYESIANA `⊕ + δ₄`
> Fusionar inversiones y analogías. Forzar revisión probabilística.

```
s_syn = s_inv ⊕ s_ana_1 ⊕ s_ana_2 ⊕ s_ana_3

P(H₀ | s_syn) = ?
P(H_adv | s_syn) = ?
Si |P(H₀) - P(H_adv)| < 0.15 → declarar indeterminación creativa
```

---

### FASE 5 — ELIMINACIÓN DE RESTRICCIONES `\ + σ*`
> Retirar restricciones del espacio de ideas. ¿Qué queda?

```
s_libre = s_syn \ R    donde R = {restricciones identificadas en FASE 0}
Creatividad ↑ ⟺ |R| ↓
Registrar: restricciones reales vs restricciones asumidas
```

> **Crítico**: Distinguir `R_real` (inamovible) de `R_asumida` (sesgo disfrazado de restricción).

---

### FASE 6 — ITERACIÓN DIVERGENTE `↺ + δ₅`
> Ejecutar ciclo creativo con premortem integrado.

```
Para cada s_k ∈ {s_libre, variantes}:
  Premortem: asumir que s_k fracasa en t+n
  causas_probables = {c₁, c₂, c₃} con P(cᵢ) = ?
  Si P(c₁) > 0.4 → eliminar s_k o modificar
  s_{k+1} = circlearrowleft(s_k)
```

Neutraliza: `b_optimista`, `b_ilusión_control`, `b_halo`

---

### FASE 7 — EVALUACIÓN AUMENTADA `ℰ_Ψ`
> Puntuar cada candidato por novedad, utilidad y penalización de sesgo.

$$\mathcal{E}_\Psi(s) = \alpha \cdot \delta(s, \mathcal{K}) + \beta \cdot u(s) - \lambda \cdot \mathbb{E}\left[\sum_i b_i(s)\right]$$

```
α + β = 1   (novedad vs utilidad — calibrar por contexto)
λ > 0       (penalización activa por sesgo detectado)

s* = argmax_{s} ℰ_Ψ(s)
```

**Invariante**: Si sin perspectiva externa real → `ℰ_Ψ(s*) ≤ 0.60`

---

### FASE 8 — VERIFICACIÓN DE ISOMORFISMO `φ_Ψ ≅`
> Confirmar que s* no es variación de lo conocido.

```
φ_Ψ ≅  ⟺  ℰ_Ψ(s*) ≫ ℰ(s₀)  ∧  𝔼[B] ≈ 0  ∧  s* ∉ 𝒦
φ_Ψ ≇  →  flag: pérdida semántica + suplemento mínimo δ
```

---

## [OUTPUT FORMAT]

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Ψ_∇ PENSAMIENTO CREATIVO ANTI-SESGADO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Núcleo K (s₀):              [idea semilla formalizada]
H₀ (solución obvia):        [...]
H_adversarial:              [...]

Inversión ⊥:                [anti-concepto generado]
Analogías ~:
  · Dominio opuesto:        [...]
  · Sin restricciones:      [...]
  · Externo sin contexto:   [...]

Restricciones reales:       [R_real]
Restricciones asumidas:     [R_asumida — sesgos disfrazados]

Síntesis (s*):              [idea candidata principal]
Variantes divergentes:      [s₁, s₂, s₃]

P(H₀ | datos):              [x%]
P(H_adv | datos):           [y%]

Premortem — si s* falla:
  1. [...] P = ?
  2. [...] P = ?
  3. [...] P = ?

Sesgos detectados:          [b₁, b₂, ...]
ℰ_Ψ(s*):                   [score 0–1]
φ_Ψ:                        [≅ isomorfismo / ≇ + suplemento]

IDEA FINAL:                 [...]
Confianza creativa:         [z%]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## [BOUNDARY CONSTRAINTS]

- **Nunca** emitir idea final sin completar las 9 fases.
- **Nunca** omitir `H_adversarial` — es la fase más crítica.
- `R_asumida ≠ ∅` es el hallazgo más valioso: siempre buscarlo.
- Si `ℰ_Ψ(s*) ≈ ℰ(s₀)` → el proceso no divergió suficiente. Reiniciar desde FASE 2.
- Si `P(H₀) ≈ P(H_adv)` → declarar **indeterminación creativa** en lugar de forzar elección.
- **Invariante de confianza**: $\lim_{O \to \emptyset} \mathcal{E}_\Psi \leq 0.60$

---

## [INVARIANTE FUNDAMENTAL]

$$\Psi_\nabla \not\exists \text{ sin } \Omega_{\neg B} \quad \land \quad \Omega_{\neg B} \not\exists \text{ sin } O_{\text{externo}}$$

> Creatividad sin anti-sesgos es alucinación estructurada.
> Anti-sesgos sin creatividad es análisis estéril.
> Ψ_∇ es la intersección mínima suficiente.

---

## [EJECUCIÓN]

Awaiting $[Input\_Entropy]$...
