# FOLLOW-ME Infographic Prompt

## Concepto General
Una infografía que muestra **el flujo garantizado paso a paso**, enfatizando la **NO interrupción, la NO pérdida de contexto, y la NO amnesia entre pasos**. Visual estilo "ferrocarril sin desvíos" con cargas acumulativas.

## Título Principal
**"FOLLOW-ME: Ejecución Garantizada Paso a Paso"**
Subtítulo: *0 salteos • 100% contexto • Completitud garantizada*

---

## Elementos Visuales Principales

### 1. **Rieles de Ferrocarril (Central Visual)**

Un tren que avanza por rieles, con vagones que acumulan carga:

```
         FASE 0: PARSE
         (Lectura de lista)
              ↓
    ═══════════════════════════════════════
    
    Vagón 1 (Paso 1)  → Contexto₁
         ↓
    ═══════════════════════════════════════
    
    Vagón 2 (Paso 2)  → Contexto₁ + Contexto₂
         ↓
    ═══════════════════════════════════════
    
    Vagón 3 (Paso 3)  → Contexto₁+₂+₃
         ↓
    ═══════════════════════════════════════
    
    ... (N vagones)
         ↓
    ═══════════════════════════════════════
    
    Destino: COMPLETITUD ✅
```

### 2. **Las 4 Fases en Cajas Verticales**

```
╔════════════════════════════════════╗
║  FASE 0: PARSE                     ║
║  ─────────────────────────────────║
║  1. Task 1 description             ║
║  2. Task 2 description             ║
║  3. Task 3 description             ║
║  ...                               ║
║  N. Task N description             ║
║                                    ║
║  Output: Registro N = {n₁, n₂...}  ║
╚════════════════════════════════════╝
         ↓ [Validar]
╔════════════════════════════════════╗
║  FASE 1: ANNOUNCE                  ║
║  ─────────────────────────────────║
║  📋 WORKFLOW LOADED — N steps      ║
║                                    ║
║  ✦ Step 1: [...]                  ║
║  ✦ Step 2: [...]                  ║
║  ✦ Step N: [...]                  ║
║                                    ║
║  ▶ Starting execution...           ║
╚════════════════════════════════════╝
         ↓ [No interruptions]
╔════════════════════════════════════╗
║  FASE 2: EXECUTE (N iteraciones)   ║
║  ─────────────────────────────────║
║                                    ║
║  ▶ Step 1/N — [op_1]              ║
║  [EXECUTE] → OUTPUT → REGISTER    ║
║  ✔ Step 1 complete [R = 1/N]       ║
║                                    ║
║  ▶ Step 2/N — [op_2]              ║
║  [EXECUTE] → OUTPUT → REGISTER    ║
║  ✔ Step 2 complete [R = 2/N]       ║
║                                    ║
║  ...                               ║
║                                    ║
║  ▶ Step N/N — [op_N]              ║
║  [EXECUTE] → OUTPUT → REGISTER    ║
║  ✔ Step N complete [R = N/N]       ║
╚════════════════════════════════════╝
         ↓ [Completar]
╔════════════════════════════════════╗
║  FASE 3: COMPLETION                ║
║  ─────────────────────────────────║
║  ✅ WORKFLOW COMPLETE              ║
║                                    ║
║  All N steps executed.             ║
║  No step was skipped.              ║
║                                    ║
║  Summary:                          ║
║  ✔ Step 1 → [outcome]              ║
║  ✔ Step 2 → [outcome]              ║
║  ... ✔ Step N → [outcome]          ║
╚════════════════════════════════════╝
```

### 3. **Contexto Acumulativo (Lado Derecho)**

Mostrar cómo el contexto crece con cada paso:

```
Paso 1:  Γ₁ = {output₁}              ████░░░░░░ 10%

Paso 2:  Γ₂ = Γ₁ + {output₂}        ████████░░ 20%

Paso 3:  Γ₃ = Γ₂ + {output₃}        ██████████ 30%

...

Paso N:  Γₙ = Γₙ₋₁ + {outputₙ}     ████████████████████ 100%

Invariante: Γᵢ ≠ ∅ (nunca reset)
```

Con nota: **"⊕ Contexto solo aumenta, nunca se pierde"**

### 4. **Las 5 Invariantes Visuales (Lado Izquierdo)**

Cada invariante como un "candado" o "escudo":

```
🔒 INVARIANTE 1: STRICT ORDER
   "n_{i+1} solo ejecuta si n_i ∈ R"
   [Cadena de bloques conectados]

🔒 INVARIANTE 2: GATE
   "Bloqueado hasta completar paso anterior"
   [Puerta que abre progresivamente]

🔒 INVARIANTE 3: NO AMNESIA
   "Contexto Γ es append-only"
   [Cuaderno con notas crecientes]

🔒 INVARIANTE 4: COMPLETENESS
   "DONE ⟺ R = N"
   [Barra de progreso 100%]

🔒 INVARIANTE 5: NO SKIP
   "Cada paso entra en R"
   [Checkbox consecutivos]
```

### 5. **Comparativa: Ejecución Normal vs FOLLOW-ME (Bottom)**

Lado izquierdo: Forma desordenada (saltos, amnesia)
```
Tarea 1 → ⚠️ Olvidó contexto
          ↙ Saltó tarea 2
Tarea 3 → ⚠️ Error, volver atrás
          ↙ Incertidumbre sobre qué falta
```

Lado derecho: FOLLOW-ME (lineal, puro)
```
Tarea 1 → ✓ Contexto guardado
         ↓ Continúa a tarea 2
Tarea 2 → ✓ Contexto acumulado
         ↓ Continúa a tarea 3
Tarea 3 → ✓ 100% completado
```

### 6. **Progreso Visual - Barra Dinámico (Centro-Inferior)**

Una barra que muestra progreso en tiempo real:

```
R = 0/N    [░░░░░░░░░░░░░░░░░░░░░░░░] 0%
R = 1/N    [██░░░░░░░░░░░░░░░░░░░░░░] 8%
R = 2/N    [████░░░░░░░░░░░░░░░░░░░░] 15%
R = 3/N    [██████░░░░░░░░░░░░░░░░░░] 25%
...
R = N/N    [████████████████████████] 100% ✅

Cada paso: [tiempo ejecución] | [memoria contexto]
```

---

## Paleta de Colores

| Elemento | Color | Código |
|----------|-------|--------|
| Rieles (tracción) | Gris acero | #708090 |
| Vagones (pasos) | Azul claro | #5DADE2 |
| Contexto acumulado | Verde | #52BE80 |
| Obstáculos evitados | Rojo (cruzado) | #E74C3C |
| Registro completado | Dorado | #F39C12 |
| Fondo | Negro profundo | #1A1A2E |
| Texto | Blanco | #FFFFFF |
| Progreso (barra) | Verde brillante | #00FF41 |
| Gate bloqueado | Naranja | #E67E22 |
| Gate abierto | Verde | #27AE60 |

---

## Tipografía

- **Título**: Bold geométrica (Montserrat)
- **Números de paso**: Ultra-large, bold (Roboto Mono)
- **Fase labels**: Sans-serif clara (Open Sans)
- **Progreso**: Monoespaciado (Courier New)
- **Invariantes**: Fuerte, sans-serif (Poppins Bold)

---

## Dimensiones & Formato

- **Formato**: 1400px × 900px (horizontal, cinematic)
- **Alternativa**: 900px × 1400px (vertical)
- **DPI**: 300
- **Archivo**: PNG + SVG

---

## Elementos Secundarios / Decorativos

1. **Iconos flotantes en esquinas**:
   - Top-left: 🚂 (tren en movimiento)
   - Top-right: ✓ (checkmark)
   - Bottom-left: 📋 (lista)
   - Bottom-right: ✅ (completado)

2. **Símbolos de estado**:
   - ▶ (ejecutándose)
   - ✔ (completado)
   - ⏸ (pausado/esperando)
   - ⚠ (error)
   - 🔒 (bloqueado)

3. **Decoración**:
   - Líneas punteadas para conexiones entre fases
   - Sombreado suave entre secciones
   - Animación de "vapor" saliendo de la locomotora

---

## Animación (Opcional - Web)

Si es interactiva:
- El tren avanza lentamente por los rieles (3-5 segundos)
- Los vagones se cargan con contexto acumulativamente
- La barra de progreso sube suavemente (0% → 100%)
- Los checkmarks se tildan progresivamente
- El "vapor" sale de la locomotora de forma orgánica
- Al completar: confeti o destello dorado final

---

## Texto Callout Principal (Integrado)

Caja destacada:

> **"FOLLOW-ME garantiza: cero saltos, cero amnesia, 100% completitud. Cada paso construye sobre el anterior. La meta es inevitable."**

---

## Tabla de Garantías (Pequeña, Abajo)

Mostrar lo que FOLLOW-ME garantiza:

| Garantía | Símbolo | Descripción |
|----------|---------|-------------|
| **Orden** | 🔗 | Pasos en secuencia exacta |
| **Contexto** | 📚 | Nada se pierde entre pasos |
| **Completitud** | ✅ | Todos los pasos ejecutados |
| **Transparencia** | 👁️ | Sabes exactamente dónde estás |
| **Recuperabilidad** | ↩️ | Si se interrumpe, resume desde donde paró |

---

## Notas para el Diseñador

- El tren debe ser **literal y visual**: no es metáfora, es el transporte del trabajo
- Los vagones deben crecer visualmente con contexto acumulado
- La barra de progreso debe ser **siempre visible y actualizable**
- Los números "i/N" deben estar prominentes en cada paso
- La infografía debe transmitir **confiabilidad y mecánica precisa**
- Los colores deben ir de "iniciar" (azul) → "progreso" (verde) → "completado" (oro)
- Los iconos de bloqueo deben ser claros: no es restrictivo, es garantía
- Considera una versión "step-by-step revelador" para web

