# Logic Skills Library

Una colección de skills avanzadas de razonamiento y pensamiento para Claude, diseñadas para mejorar la capacidad de análisis, formalización, creatividad y ejecución sistemática.

## 📚 Habilidades disponibles

### 1. **K-Logic** — Motor de Formalización Universal

![K-Logic Infographic](docs/infografias/k-logic.png)

Traduce cualquier input en su representación matemática/lógica más fundamental usando sintaxis LaTeX estricta.

**Cuándo usarlo:**
- Necesitas formalizar conceptos abstractos o verbosos
- Quieres reducir un argumento a su núcleo lógico puro
- Requieres expresiones matemáticas rigurosas
- Buscas comprimir información de alta entropía

**Triggers:**
- "usa k-logic"
- "activa k-logic"
- "formaliza esto"
- "reduce a lógica"
- "exprésalo matemáticamente"
- "minimaliza esto"

**Protocolo:** 4 fases
1. **IDENTIFY** — Extraer variables y predicados
2. **PURIFY** — Filtrar ruido lingüístico
3. **FORMALIZE** — Mapear a dominio matemático apropiado
4. **VERIFY** — Confirmar isomorfismo sin pérdida de significado

**Casos de uso:**
- 🔬 **Investigación**: Formalizar una hipótesis científica compleja en ecuaciones
- 💼 **Negocios**: Reducir una estrategia comercial a variables clave y restricciones
- 🏛️ **Legal/Compliance**: Expresar requisitos regulatorios como predicados lógicos
- 🧠 **Filosofía**: Convertir argumentos abstractos en lógica de primer orden
- 🏗️ **Ingeniería**: Especificar sistemas complejos con notación formal
- 📊 **Análisis de datos**: Transformar preguntas verbosas en consultas matemáticas

**Ejemplo:**
```
Input: "Los clientes satisfechos compran más y recomiendan la empresa a otros"
Output K-Logic:
  S(x) = cliente satisfecho
  P(x) = compra más
  R(x) = recomienda
  ∀x: S(x) ⟹ (P(x) ∧ R(x))
```

---

### 2. **Ω_¬B (Omega Anti-Sesgos)** — Motor de Razonamiento Imparcial

![Omega Anti-Sesgos Infographic](docs/infografias/omaga-antisesgos.png)

Minimiza sistemáticamente sesgos cognitivos antes de emitir análisis, juicios o decisiones mediante una cadena de pensamiento estructurada en 7 fases.

**Cuándo usarlo:**
- Necesitas máxima objetividad en análisis
- Estás evaluando personas, proyectos o inversiones
- Requieres decisiones importantes sin sesgos
- Quieres análisis crítico imparcial

**Triggers:**
- "usa omega"
- "activa omega-antisesgos"
- "analiza sin sesgos"
- "razona sin sesgos"
- "aplica antisesgos"
- "quiero análisis imparcial"

**Protocolo:** 7 fases
1. **REGISTRO PREVIO** — Pre-registrar hipótesis antes de analizar
2. **PURIFICACIÓN** — Separar datos de interpretación
3. **ADVERSARIAL** — Construir argumento contrario más fuerte
4. **DIVERSIDAD COGNITIVA** — Simular 3+ perspectivas distintas
5. **ACTUALIZACIÓN BAYESIANA** — Asignar probabilidades formales
6. **PREMORTEM** — Asumir error e identificar causas
7. **SKIN IN THE GAME** — Verificar consecuencias reales

**Output:** Juicio final con confianza porcentual y análisis de sesgos detectados

**Casos de uso:**
- 👤 **RRHH**: Evaluar candidatos sin sesgos de género, edad o procedencia
- 💰 **Inversión**: Analizar startups sin sesgo de novedad o trends actuales
- ⚖️ **Toma de decisiones**: Evaluar propuestas laborales sin desperación o euforia
- 📈 **Product**: Revisar críticas de usuarios/competencia imparcialmente
- 🎯 **Selección de proveedores**: Comparar opciones sin favoritismos previos
- 🔍 **Due diligence**: Investigar antes de grandes cambios organizacionales
- 📰 **Fact-checking**: Evaluar claims sin sesgo confirmatorio

**Ejemplo:**
```
Evaluación: "¿Es X un buen candidato para el puesto?"

H₀ (prejuicio esperado): Es joven, graduado recientemente, probablemente bueno
H_adversarial: Falta experiencia, puede irse rápido, caro de capacitar

→ Análisis separado sin emociones
→ P(H₀|datos) = 65%, P(H_adv|datos) = 35%
→ Confianza final: 62% (máxima permitida sin perspectiva externa completa)
```

---

### 3. **Ψ_∇ (Psi Divergente)** — Motor de Pensamiento Creativo Anti-Sesgado

![Psi Divergente Infographic](docs/infografias/omaga-divergente.png)

Fusiona creatividad divergente, razonamiento anti-sesgos y formalización K-Logic para generar ideas genuinamente novedosas mientras elimina sistemáticamente los sesgos que distorsionan el juicio creativo.

**Cuándo usarlo:**
- Necesitas creatividad rigurosa con máxima novedad
- Requieres brainstorming de alto riesgo
- Buscas diseño de sistemas novedosos
- Quieres evaluar ideas propias vs externas sin sesgo
- Necesitas arquitectura de productos/negocios genuinamente original

**Triggers:**
- "usa omega-divergente"
- "activa omega-divergente"
- "piensa sin sesgos creativos"
- "genera ideas radicales"
- "diverge sin sesgo"
- "quiero pensamiento creativo riguroso"

**Protocolo:** 9 fases
1. **PURIFICACIÓN K** — Reducir input a núcleo semántico formal
2. **REGISTRO PREVIO** — Pre-registrar hipótesis creativa
3. **INVERSIÓN** — Negar supuesto central
4. **ANALOGÍA DIVERSA** — Mapear a dominios radicalmente distintos
5. **SÍNTESIS BAYESIANA** — Fusionar inversiones y analogías
6. **ELIMINACIÓN DE RESTRICCIONES** — Retirar restricciones asumidas
7. **ITERACIÓN DIVERGENTE** — Ciclo creativo con premortem
8. **EVALUACIÓN AUMENTADA** — Puntuar por novedad, utilidad y sesgos
9. **VERIFICACIÓN DE ISOMORFISMO** — Confirmar genuina novedad

**Output:** Idea final con score de creatividad (0-1) y confianza creativa

**Casos de uso:**
- 🚀 **Startup**: Generar modelo de negocio disruptivo sin sesgos de status quo
- 🎨 **Diseño UX/UI**: Inventar interacciones de usuario genuinamente nuevas
- 📱 **Producto**: Conceptualizar features que compitan por novedad, no por iteración
- 🏭 **Procesos**: Rediseñar workflows completos sin heredar restricciones antiguas
- 🎯 **Marketing**: Crear campañas completamente distintas a lo que "siempre funciona"
- 🔬 **Investigación**: Formular hipótesis nuevas que eviten trampa de pregunta obvia
- 💡 **Estrategia**: Pivotear empresa sin recaer en supuestos iniciales fallidos

**Ejemplo:**
```
Reto: "¿Cómo monetizamos nuestro software sin modelo de suscripción?"

Idea obvia esperada: Precio por usuario, precio por features, freemium
Inversión ⊥: Inverso = regalar el software, cobrar por algo que no es el software
Analogías ~:
  · Industria de cine: No pagas por película, pagas por acceso/comunidad
  · Teléfonos: No pagas por el teléfono, pagas por conexión
  · Restaurantes: No pagas por receta, pagas por experiencia/comunidad

Restricciones asumidas (R_asumida): 
  - "Tenemos que cobrar a quién usa el software"
  - "Todos nuestros competidores lo hacen así"
  - "No hay otra forma"

→ Idea divergente: Monetizar acceso a datos/insights, comunidad, servicios anexos
→ ℰ_Ψ score: 0.78 (novedad alta, viabilidad media)
→ Confianza: 71% (hay perspectivas externas que pueden validar)
```

---

### 4. **FOLLOW-ME** — Ejecutor Secuencial de Workflows

![FOLLOW-ME Infographic](docs/infografias/follow-me.png)

Sigue listas de tareas numeradas paso a paso, nunca saltando, manteniendo contexto completo a través de todos los pasos.

**Cuándo usarlo:**
- Tienes una lista numerada de tareas
- Quieres ejecución garantizada paso a paso
- Necesitas mantener contexto entre pasos
- Requieres que cada paso se complete antes del siguiente

**Triggers:**
- "usa follow-me"
- "activa follow-me"
- "sigue estos pasos"
- "ejecuta este workflow"
- "sigue esta lista"
- "ejecuta paso a paso"

**Protocolo:** 3 fases principales
1. **PARSE** — Analizar lista markdown numerada
2. **ANNOUNCE** — Mostrar plan completo antes de ejecutar
3. **EXECUTE** — Ejecutar cada paso en orden estricto
4. **COMPLETION** — Resumen final cuando todos los pasos terminen

**Invariantes:**
- ✓ Orden estricto (nunca saltear)
- ✓ Contexto acumulativo (nunca reset)
- ✓ Completitud (cada paso debe terminar)
- ✓ Sin preguntar entre pasos (salvo condiciones específicas)

**Casos de uso:**
- 📋 **Onboarding**: Ejecutar checklist de 15 tareas sin saltear ninguna
- 🏗️ **Migración**: Pasos secuenciales de migración de datos donde orden importa
- 🔬 **Experimento**: Protocolo científico paso a paso con contexto acumulativo
- 📚 **Tutorial**: Guía de aprendizaje donde cada paso depende de los anteriores
- 🚀 **Deployment**: Pipeline de despliegue donde un error requiere halt
- 🧪 **Testing**: Casos de prueba donde el estado anterior afecta el siguiente
- 📖 **Documentación**: Escribir documento completo en secciones ordenadas

**Ejemplo:**
```
1. Formaliza el problema (usa k-logic)
2. Analiza sin sesgos la solución anterior (usa omega)
3. Genera 3 alternativas creativas (usa omega-divergente)
4. Compara alternativas sin sesgo (usa omega nuevamente)
5. Documenta la decisión final

→ FOLLOW-ME ejecuta esto sin saltar, manteniendo contexto de K-Logic en paso 2,
  contexto de omega en paso 3, etc.
```

---

## 🎯 Matriz de Selección

| Necesidad | Skill Recomendada |
|-----------|-------------------|
| Formalizar conceptos abstractos | **K-Logic** |
| Análisis sin sesgos cognitivos | **Ω_¬B** |
| Creatividad rigurosa y original | **Ψ_∇** |
| Ejecutar lista de tareas ordenada | **FOLLOW-ME** |
| Combinar: formalización + anti-sesgos | **K-Logic + Ω_¬B** |
| Combinar: creatividad + análisis riguroso | **Ψ_∇ (incluye ambas)** |

---

## 🔗 Composición y Arquitectura

### Dependencias de Skills

```
K-Logic (núcleo de formalización)
    ↓
    ├→ Ω_¬B (anti-sesgos, usa K-Logic en FASE 0)
    │
    └→ Ψ_∇ (creatividad, usa K-Logic + Ω_¬B en paralelo)

FOLLOW-ME (ortogonal, se puede combinar con cualquiera)
```

**Combinaciones potentes:**
- **K-Logic → Ω_¬B**: Formaliza primero, analiza sin sesgos después
- **Ω_¬B → Ψ_∇**: Analiza qué no sesga, diverge creativamente desde ahí
- **FOLLOW-ME + [cualquier otra]**: Ejecuta workflow que use skills en sus pasos

---

## 📋 Estructura del Repositorio

```
logic_skills/
├── README.md                    (este archivo)
├── LICENSE                      (MIT License)
│
├── k-logic/
│   └── SKILL.md                (definición completa)
│
├── omega-antisesgos/
│   └── SKILL.md                (definición completa)
│
├── omega-divergente/
│   └── SKILL.md                (definición completa)
│
└── follow-me/
    └── SKILL.md                (definición completa)
```

---

## 🚀 Cómo usar

### Activación básica
Cada skill se activa diciendo uno de sus triggers en la conversación:

```
Usuario: "usa k-logic para formalizar este concepto"
→ Se activa K-Logic automáticamente
```

### Combinación de skills
Puedes combinarlas secuencialmente:

```
Usuario: "usa k-logic primero, luego omega para analizar sin sesgos"
→ K-Logic formaliza → Ω_¬B analiza el resultado
```

### Con FOLLOW-ME
Crea una lista numerada y especifica qué skill usar en cada paso:

```
1. Formaliza el problema (usa k-logic)
2. Analiza sin sesgos (usa omega)
3. Genera ideas alternativas (usa omega-divergente)
```

---

## 📊 Características de Output

Cada skill produce output estructurado y verificable:

| Skill | Output Principal | Métricas de Confianza |
|-------|------------------|----------------------|
| **K-Logic** | Expresión LaTeX formal | Verificación de isomorfismo (≅/≇) |
| **Ω_¬B** | Juicio + análisis de sesgos | P(H₀), P(H_adversarial), Confianza % |
| **Ψ_∇** | Idea original + variantes | ℰ_Ψ score, Confianza creativa % |
| **FOLLOW-ME** | Resumen paso a paso | Completitud (i/N) |

---

## ⚙️ Principios de Diseño

### Invariantes Universales
1. **Nunca skip**: Cada protocolo debe ejecutarse completo
2. **Adversarialidad obligatoria**: Ω_¬B y Ψ_∇ siempre generan contraargumentos
3. **Perspectiva externa**: Sin input externo real, máxima confianza limitada a 60%
4. **Contexto acumulativo**: Cada paso construye sobre los anteriores

### Sesgos Activamente Neutralizados
- Sesgo de confirmación
- Sesgo retrospectivo
- Sesgo de autoridad
- Sesgo de status quo
- Sesgo de optimismo
- Sesgo de ilusión de control
- Y 15+ más (ver SKILL.md de cada motor)

---

## 📝 Licencia

MIT License — Copyright © 2026 Ricardo M. Biot 

Libre para usar, modificar y distribuir en proyectos comerciales y personales.

---

## 🔍 Detalles Técnicos

- **Lenguaje**: Markdown + LaTeX para notación formal
- **Compatible con**: Claude, Gemini, MiniMax
- **Versión**: 1.0 (2026)
- **Mantenimiento**: Activo

---

## 💡 Ejemplos de Uso Avanzado

### Caso 1: Decisión empresarial compleja
```
FOLLOW-ME:
1. Formaliza la decisión (K-Logic)
2. Analiza sin sesgos (Ω_¬B)
3. Genera alternativas creativas (Ψ_∇)
4. Evalúa riesgos de cada una (Ω_¬B nuevamente)
```

### Caso 2: Innovación técnica
```
Ψ_∇ (Pensamiento creativo anti-sesgado)
→ Genera ideas originales + filtra sesgos en paralelo
→ Output: 3+ ideas genuinamente nuevas con premortem
```

### Caso 3: Análisis crítico de un documento
```
Ω_¬B (Anti-sesgos)
→ Separa datos de interpretaciones
→ Construye argumento adversarial más fuerte
→ Output: Evaluación rigurosa sin prejuicios
```
