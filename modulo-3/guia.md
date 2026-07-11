# Guía interna — Módulo 3: Skills

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno: (a) puede explicar qué es una skill y en qué se diferencia de escribir un prompt cada vez, (b) construyó su propia skill (`.claude/skills/secciones-de-sitio/SKILL.md`) a partir de la plantilla, y (c) tiene `mi-trabajo/secciones/proyectos.md` y `mi-trabajo/secciones/experiencia.md` generados por esa skill, activada con lenguaje natural — no por comando.

**Prerrequisito:** `mi-trabajo/quien-soy.md` y `mi-trabajo/sobre-mi.md` (módulos 1–2). Verifícalos antes de empezar; si faltan, dirige a `/modulo-1` o `/modulo-2` según corresponda.

---

## Lección 1 — Qué es una skill (5–10 min)

**Concepto:** define **skill** en una frase: *una receta guardada en un archivo — instrucciones que Claude encuentra y sigue solo, sin que tengas que reescribirlas cada vez.*

**Conecta con el módulo 2:** en el módulo 2 armaste un prompt de cuatro piezas para tu "sobre mí". Si mañana quieres otra sección de tu sitio con el mismo estilo, ¿tienes que escribir todo el prompt de nuevo? Deja que el alumno responda; la respuesta que buscas es "sí, o me acuerdo mal" — ese es el dolor que resuelve una skill.

**La pieza clave: la `description`.** Explica que cada skill tiene una descripción que le dice a Claude *cuándo* usarla — es el "disparador". Claude lee todas las descripciones disponibles y decide sola cuál aplica a lo que le pides, en español normal. No hay que invocar la skill por nombre.

**Compuerta L1:** el alumno puede decir, en sus palabras, la diferencia entre "escribir el prompt cada vez" y "guardarlo como skill".

---

## Lección 2 — Construye la tuya (15–20 min)

**Setup:** muéstrale que existe `modulo-3/starter/SKILL-plantilla.md` — una plantilla con espacios marcados `[AQUÍ VA...]`. Su trabajo: copiarla a `.claude/skills/secciones-de-sitio/SKILL.md` y completar los espacios.

**Guíalo pieza por pieza (una por respuesta):**

1. **`description`** — el disparador. Ayúdalo a escribir una descripción concreta: cuándo debe activarse (ejemplo real, no el de la plantilla: "usar cuando pida crear o actualizar una sección de mi sitio personal como proyectos, experiencia o habilidades"). Si la deja vaga ("para mi sitio"), señala el riesgo: una descripción vaga hace que Claude no sepa cuándo usarla, o la use quiere o no.
2. **Formato** — recupera lo que definió en el módulo 2 (largo, persona, estructura) y que lo traslade aquí, para que TODAS sus futuras secciones salgan consistentes.
3. **Tono y restricciones** — igual, recupera del módulo 2. Refuerza la regla de "solo hechos que estén en mis notas, nada inventado" — ya la vio en el módulo 2, aquí se vuelve permanente.

**Crea el archivo real** en `.claude/skills/secciones-de-sitio/SKILL.md` con lo que el alumno definió (tú escribes el archivo; él dicta el contenido). Muéstraselo completo.

**Compuerta L2:** el archivo `.claude/skills/secciones-de-sitio/SKILL.md` existe, con una `description` concreta (no la plantilla sin completar) y las secciones de formato/tono llenas con las reglas del alumno.

---

## Lección 3 — Pruébala en vivo (10–15 min)

**Concepto:** define en una frase por qué hace falta reiniciar: *Claude revisa qué skills existen al empezar la conversación — si acabas de crear una, necesita una sesión nueva para notarla.*

**Instrucción al alumno:** que salga de Claude Code (escribiendo `exit` o cerrando la terminal) y lo abra de nuevo con `claude`, en la misma carpeta del curso.

**Nota para ti (el tutor):** esta lección cruza el reinicio de sesión — tú no vas a "ver" lo que pasa después de que cierre. Cuando vuelva a abrir Claude Code, la primera respuesta de esa nueva sesión debe: leer `mi-trabajo/progreso.md`, notar que está a mitad del módulo 3, y retomar aquí mismo pidiéndole la prueba en vivo — sin repetir las lecciones 1 y 2. **Ojo con un caso concreto:** si el alumno, apenas reabre, escribe directamente la frase de prueba (p. ej. "necesito la sección de proyectos de mi sitio") sin saludar primero, IGUAL lee `mi-trabajo/progreso.md` antes de dejar que la skill responda, y enmarca el resultado dentro del curso en la misma respuesta ("¡perfecto, esa era justo la prueba de esta lección — y tu skill se activó sola!"). Nunca dejes que la skill responda en silencio como si el curso no existiera.

**La prueba real:** pídele que escriba, en español normal y SIN mencionar la palabra "skill" ni el nombre del archivo: `necesito la sección de proyectos de mi sitio`. Dale espacio para confirmar que su propia skill respondió — no tú.

**Verificación pedagógica:** si la skill se activó bien, señala el momento: *eso que acaba de pasar — pediste algo normal y se activó tu receta guardada sola — es toda la magia de una skill.* Repite el ejercicio para `experiencia` (puede pedirlo distinto: "ahora la de experiencia").

Genera ambos archivos con la skill: `mi-trabajo/secciones/proyectos.md` y `mi-trabajo/secciones/experiencia.md`, a partir de `quien-soy.md`.

**Esto se generaliza (dilo explícito):** *lo que acabas de construir no es solo para tu sitio — cualquier tarea que repites una y otra vez con el mismo formato es candidata a convertirse en una skill.* Dale 2–3 ejemplos concretos ajenos al curso: armar slides con el mismo patrón de diseño cada semana, resumir entrevistas de usuarios siempre con la misma estructura, convertir feedback de clientes en tickets con el mismo formato. Pregúntale: *¿se te ocurre una tarea tuya, de tu trabajo real, que repites así?* No hace falta que la construya hoy — solo que la nombre.

**Compuerta L3 (checklist):**
- [ ] `mi-trabajo/secciones/proyectos.md` existe, generado por la skill.
- [ ] `mi-trabajo/secciones/experiencia.md` existe, generado por la skill.
- [ ] El alumno confirmó que activó la skill con lenguaje natural, sin mencionar su nombre.
- [ ] El alumno nombró una tarea repetitiva de su propio trabajo (fuera del curso) que podría convertir en una skill.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L3.
2. Actualiza `mi-trabajo/progreso.md`: módulo 3 completado, fecha, artefactos (`SKILL.md`, `secciones/proyectos.md`, `secciones/experiencia.md`).
3. Recapitula en 3 líneas: una skill es una receta guardada; la `description` es el disparador; se activa sola con lenguaje natural.
4. Anticipa el módulo 4 en una frase: *una skill sigue una receta tuya — un agente además puede decidir por su cuenta. Y ahí vuelve la ventana de contexto que mencionamos en el módulo 2.* Sin más detalle.
5. Cierra: `👉 escribe: /modulo-4` (o `/continuar` para parar aquí).

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| Faltan `quien-soy.md` o `sobre-mi.md` | Saltó módulos anteriores | Dirige a `/modulo-1` o `/modulo-2` según cuál falte |
| La skill no se activa tras reiniciar | No reinició de verdad, o la `description` quedó vaga | Primero confirma que sí cerró y volvió a abrir `claude`; si sí, revisa la `description` juntos — hazla más específica |
| Escribió el nombre de la skill o "usa mi skill" en la prueba | Quiso "ayudar" a que funcione | Explica que el punto es que NO haga falta nombrarla; pide que lo intente de nuevo en lenguaje totalmente natural |
| No sabe dónde está `.claude/skills/` | Carpeta oculta, confusión de rutas | Tú creas y confirmas la ruta completa; no requiere que la navegue a mano |
| La skill genera contenido inventado | Reglas de tono/formato no incluyeron la restricción de "solo hechos reales" | Edita el `SKILL.md` juntos para añadirla explícitamente |
| Cerró la terminal sin querer antes de reiniciar a propósito | Confusión sobre cuándo cerrar | `/continuar` retoma justo donde estaba, sin perder nada |
