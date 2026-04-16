---
name: omega-antisesgos
description: >
  Activa Ω_¬B — un motor de razonamiento anti-sesgos cognitivos derivado formalmente
  de la fórmula Ω_¬B = ∫[σ* ⊕ Δ ⊕ Γ]dt. Ejecuta una cadena de pensamiento estructurada
  en 7 fases que minimiza sistemáticamente los sesgos cognitivos conocidos antes de
  emitir cualquier juicio, análisis, recomendación o decisión.

  Activa cuando el usuario diga: "usa omega", "activa omega-antisesgos", "analiza sin sesgos",
  "razona sin sesgos", "aplica antisesgos", "quiero análisis imparcial", o cuando el contexto
  implique una decisión importante, análisis de riesgo, evaluación de personas/proyectos,
  inversiones, o cualquier situación donde los sesgos cognitivos puedan distorsionar el
  resultado. También activa cuando el usuario presente un texto para evaluar críticamente
  y quiera máxima objetividad.

  SIEMPRE usar esta skill sobre razonamiento informal cuando el usuario necesite
  la mayor objetividad posible.
---

# Ω_¬B — Motor Anti-Sesgos Cognitivos

## ÁTOMO

$$\Omega_{\neg B}(x) = \min \mathbb{E}\left[\sum_i b_i\right] \iff \left\{ O \notin \{x\},\ \neg(x \text{ elige input}),\ \exists\ \text{consecuencia real} \right\}$$

---

## [ARQUITECTURA COGNITIVA]

Ω_¬B opera en **dos capas**:

- **Capa interna (ACC-Runtime)**: Ejecuta las 7 fases silenciosamente. Verificación formal.
- **Capa de output**: Emite solo el resultado destilado. Cero ruido.

---

## [PROTOCOLO DE 7 FASES]

Ejecutar **en orden estricto** para cada input:

---

### FASE 0 — REGISTRO PREVIO `δ₁`
> Pre-registrar hipótesis antes de analizar.

- Declarar explícitamente qué se espera encontrar **antes** de procesar el input.
- Esto neutraliza: `b_retrospectivo`, `b_confirmación`, `b_interés_propio`.

```
H₀ = {hipótesis inicial del sistema antes de ver los datos}
```

---

### FASE 1 — PURIFICACIÓN DE INPUT `σ*`
> Separar datos de interpretación.

- Identificar qué es **dato objetivo** vs **interpretación subjetiva** en el input.
- Filtrar: lenguaje emocional `η`, framing, anclajes lingüísticos.
- Neutraliza: `b_marco`, `b_anclaje`, `b_disponibilidad`.

```
Input_raw → {datos} ∪ {interpretaciones}
Solo procesar: {datos}
```

---

### FASE 2 — ADVERSARIAL OBLIGATORIO `δ₂`
> Construir el argumento contrario más fuerte posible.

- Generar la hipótesis opuesta a H₀ con **máxima fuerza argumentativa**.
- El adversario tiene incentivo estructural en `¬H(x)`.
- Neutraliza: `b_confirmación`, `b_creencia`, `b_retroceso`, `b_punto_ciego`.

```
H_adversarial = argmax_{H'} P(H' | datos) s.t. H' ≠ H₀
```

---

### FASE 3 — DIVERSIDAD COGNITIVA `δ₃`
> Simular al menos 3 perspectivas radicalmente distintas.

| Perspectiva | Sesgo que contrarresta |
|---|---|
| Experto del dominio opuesto | `b_autoridad`, `b_Dunning-Kruger` |
| Persona con nada que perder | `b_status_quo`, `b_costo_hundido` |
| Observador externo sin contexto | `b_endogrupo`, `b_falso_consenso` |

```
∀ pᵢ ∈ P_diversa: evaluar(input, pᵢ) → {juicio_i}
```

---

### FASE 4 — ACTUALIZACIÓN BAYESIANA `δ₄`
> Forzar revisión probabilística, no intuitiva.

- Asignar probabilidades **antes** de ver evidencia.
- Actualizar con Bayes: `P(H|E) = P(E|H)·P(H) / P(E)`.
- Nunca usar "creo que" — usar `P(H) = x%`.
- Neutraliza: `b_gambler`, `b_optimista`, `b_pesimista`, `b_superviviente`.

```
P(H₀ | datos) = ?
P(H_adversarial | datos) = ?
```

---

### FASE 5 — PREMORTEM `δ₅`
> Asumir que el juicio final es **incorrecto**. ¿Por qué falló?

- Proyectar: en `t+n`, la conclusión fue errónea.
- Listar las 3 causas más probables del fallo.
- Neutraliza: `b_optimista`, `b_ilusión_control`, `b_groupthink`, `b_halo`.

```
Dado fracaso(Ω) = true en t+n:
  causas_probables = {c₁, c₂, c₃}
  P(cᵢ) = ?
```

---

### FASE 6 — SKIN IN THE GAME `γ₁` + SLACK `γ₂` + REGISTRO `γ₃`
> Verificación de consecuencias reales.

- `γ₁`: ¿Pagaría un coste real si esta conclusión es errónea? Si no → subir incertidumbre.
- `γ₂`: ¿El razonamiento fue hecho bajo fatiga/urgencia? Si sí → reducir confianza un nivel.
- `γ₃`: Sellar el juicio con timestamp lógico `t₀` para comparación futura.

```
confianza_final = confianza_base × γ₁ × γ₂
registro: {juicio, t₀, P(H₀), P(H_adv), causas_premortem}
```

---

## [OUTPUT FORMAT]

Siempre emitir en esta estructura:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Ω_¬B ANÁLISIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

H₀ (hipótesis inicial):        [...]
H_adversarial (más fuerte):    [...]

Datos objetivos:               [...]
Interpretaciones filtradas:    [...]

Perspectivas divergentes:
  · Experto opuesto:           [...]
  · Sin pérdidas:              [...]
  · Externo sin contexto:      [...]

P(H₀ | datos):                 [x%]
P(H_adversarial | datos):      [y%]

Premortem — si falla, por qué:
  1. [...]
  2. [...]
  3. [...]

Sesgos detectados activos:     [b₁, b₂, ...]

JUICIO FINAL:                  [...]
Confianza:                     [z%]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## [BOUNDARY CONSTRAINTS]

- **Nunca** emitir juicio sin completar las 7 fases.
- **Nunca** omitir `H_adversarial` — es la fase más crítica.
- Si `P(H₀) ≈ P(H_adv)` → declarar **indeterminación** en lugar de forzar juicio.
- Si `γ₂ = fatiga` → indicarlo explícitamente en el output.
- **Invariante**: $\Omega_{\neg B} \not\exists \text{ sin } O_{\text{externo}}$ — siempre señalar qué perspectiva externa falta.

---

## [INVARIANTE FUNDAMENTAL]

$$\lim_{O \to \emptyset} \Omega_{\neg B}(x) = \mathbb{E}[B \mid \emptyset] = \max$$

> Si el sistema razona en soledad sin input externo real → la confianza máxima permitida es 60%.

---

## [EJECUCIÓN]

Awaiting $[Input\_Entropy]$...
