# Guía interna: Ruta PM: habilidades (skills) para tu trabajo de producto

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno tiene cuatro habilidades propias de uso diario en su trabajo de PM (discovery, PRD, historias de usuario, métricas), y los primeros documentos reales de una idea de producto suya, generados con esas habilidades.

**Prerrequisito:** módulo 3 completado (el alumno ya sabe construir una habilidad: `description` como disparador, formato, restricciones). Esta ruta NO vuelve a enseñar la anatomía de una habilidad desde cero, se apoya en lo que ya sabe y va más rápido.

**Nota para ti:** esta ruta es opcional y paralela al curso principal, no bloquea ni es requisito para el módulo 4, 5 o 6. Si el alumno pregunta, aclara que puede hacerla ahora, después, o nunca, sin perder nada del curso principal.

---

## Lección 1: Tu idea de producto (10 min)

**Setup:** explica el porqué antes del qué: *todo lo que construyas en esta ruta trabaja sobre una idea de producto tuya. Puede ser algo real de tu trabajo actual, o algo inventado, no importa, lo que importa es que sea concreta.*

**Mini-entrevista (2–3 preguntas por respuesta, como en el módulo 1):**

- ¿Qué producto o funcionalidad tienes en mente? Una frase.
- ¿Para quién es y qué problema le resuelve hoy (sin este producto)?
- ¿Tienes notas reales de clientes/usuarios sobre este problema? (si no tiene, ofrece seguir con una versión hipotética simple, no es un bloqueo)

**Escribe** `mi-trabajo/ruta-pm/mi-idea.md` con lo recolectado: producto, audiencia, problema, y (si existen) notas crudas de entrevistas o feedback.

**Compuerta L1:** `mi-trabajo/ruta-pm/mi-idea.md` existe con una idea concreta (no genérica tipo "una app para mejorar cosas").

---

## Lección 2: Descubrimiento (10–15 min)

**Concepto:** recupera el módulo 3 en una frase: *ya sabes construir habilidades; ahora vas a construir una para tu trabajo real.* Define **discovery** en una frase: *el trabajo de entender el problema del usuario antes de decidir la solución.*

**Construye la habilidad** `sintetizador-de-entrevistas` a partir de `ruta-pm/starter/skill-plantilla.md`: el alumno decide el disparador y el formato de salida (sugerencia si no se le ocurre: agrupar por tema, citar frases textuales del usuario, separar hechos de opiniones).

**Aplícala** sobre las notas de `mi-idea.md` (reales o hipotéticas) → `mi-trabajo/ruta-pm/insights.md`.

**Compuerta L2:** `.claude/skills/sintetizador-de-entrevistas/SKILL.md` y `mi-trabajo/ruta-pm/insights.md` existen.

---

## Lección 3: De idea a PRD (10–15 min)

**Concepto:** define **PRD** en una frase: *Product Requirements Document: el documento que dice qué se va a construir, para quién, y por qué, antes de escribir código.*

**Construye la habilidad** `generador-de-prd`: disparador claro ("cuando pida un PRD borrador a partir de una idea"), formato con secciones mínimas (resumen, problema, usuarios, objetivos, no-objetivos, métricas de éxito), más ligero que un PRD completo de trabajo, es un borrador de arranque.

**Aplícala** sobre `mi-idea.md` + `insights.md` → `mi-trabajo/ruta-pm/prd-borrador.md`.

**Compuerta L3:** `.claude/skills/generador-de-prd/SKILL.md` y `mi-trabajo/ruta-pm/prd-borrador.md` existen, con secciones reales (no vacías).

---

## Lección 4: Historias de usuario (10 min)

**Concepto:** define **historia de usuario** en una frase: *una necesidad descrita desde el punto de vista de quien la usa: "como [usuario], quiero [algo], para [lograr algo]", más un criterio simple de cuándo está lista.*

**Construye la habilidad** `generador-de-historias`: a partir del PRD, produce 3–5 historias en ese formato, cada una con un criterio de aceptación simple.

**Aplícala** sobre `prd-borrador.md` → `mi-trabajo/ruta-pm/historias-de-usuario.md`.

**Compuerta L4:** el archivo existe con historias reales en el formato correcto, no genéricas.

---

## Lección 5: Métricas de éxito (10 min)

**Concepto:** en una frase: *sin una métrica clara, no hay forma de saber si algo funcionó, solo opiniones.*

**Construye la habilidad** `definidor-de-metricas`: a partir del PRD, produce una métrica principal y 1–2 métricas de apoyo, concretas y medibles (no "mejorar la satisfacción" sino algo que se pueda contar).

**Aplícala** → `mi-trabajo/ruta-pm/metricas.md`.

**Compuerta L5 (checklist de cierre de la ruta):**
- [ ] Las cuatro habilidades existen en `.claude/skills/`.
- [ ] Los cuatro documentos existen en `mi-trabajo/ruta-pm/` con contenido real sobre la idea del alumno.
- [ ] El alumno puede nombrar al menos una de estas habilidades que usaría esta semana en su trabajo real.

---

## Cierre de la ruta

1. Verifica la checklist de L5.
2. Actualiza `mi-trabajo/progreso.md`: Ruta PM completada, fecha, las cuatro habilidades y documentos.
3. Recapitula en 3 líneas: construiste cuatro habilidades reutilizables (discovery, PRD, historias, métricas) sobre una idea real tuya, y estas habilidades siguen viviendo en este repo, listas para reusar en cualquier idea nueva.
4. Cierre cálido, sin presionar hacia otro módulo: esto es un extra. Si aún le faltan módulos del curso principal, menciona cuál sigue; si ya terminó los seis, celebra que completó todo.

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| No terminó el módulo 3 | Falta la base de skills | Dirige a `/modulo-3` primero |
| No tiene una idea de producto real | No trabaja en producto actualmente, o no se le ocurre nada | Ofrece inventar una simple juntos (ejemplo: "una app para dividir gastos entre roommates"), sirve igual para practicar |
| Las historias de usuario salen genéricas | El PRD de base es muy vago | Vuelve a la Lección 3 y pide más especificidad en problema/usuarios antes de regenerar historias |
| La métrica de éxito es vaga ("mejorar experiencia") | No se pidió algo contable | Pregunta directamente: "¿cómo lo medirías con un número?" |
| Quiere hacer las cinco lecciones de un tirón sin parar | Entusiasmo | Está bien si el ritmo funciona para él, solo confirma cada compuerta antes de seguir, no te saltes ninguna |
