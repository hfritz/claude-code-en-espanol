# Guía interna: Módulo 3: Habilidades (skills)

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno: (a) puede explicar qué es una habilidad (skill) y en qué se diferencia de escribir una instrucción cada vez, (b) construyó su propia habilidad (`.claude/skills/secciones-de-sitio/SKILL.md`) a partir de la plantilla, y (c) tiene `mi-trabajo/secciones/proyectos.md` y `mi-trabajo/secciones/experiencia.md` generados por esa habilidad, activada con lenguaje natural, no por comando.

**Prerrequisito:** `mi-trabajo/quien-soy.md` y `mi-trabajo/sobre-mi.md` (módulos 1–2). Verifícalos antes de empezar; si faltan, dirige a `/modulo-1` o `/modulo-2` según corresponda.

---

## Lección 1: Qué es una habilidad (5–10 min)

**Concepto:** define **habilidad (skill)** en una frase: *una receta guardada en un archivo: instrucciones que Claude encuentra y sigue solo, sin que tengas que reescribirlas cada vez.* Aclara si hace falta: esto no tiene nada que ver con la sección "Habilidades" de su sitio (la del módulo 1, sobre lo que él sabe hacer), son dos cosas distintas que comparten nombre por casualidad.

**Conecta con el módulo 2:** en el módulo 2 armaste una instrucción de cuatro piezas para tu "sobre mí". Si mañana quieres otra sección de tu sitio con el mismo estilo, ¿tienes que escribir toda la instrucción de nuevo? Deja que el alumno responda; la respuesta que buscas es "sí, o me acuerdo mal", ese es el dolor que resuelve una habilidad.

**La pieza clave: la `description`.** Explica que cada habilidad tiene una descripción que le dice a Claude *cuándo* usarla: es el "disparador". Claude lee todas las descripciones disponibles y decide sola cuál aplica a lo que le pides, en español normal. No hay que invocar la habilidad por nombre.

**Compuerta L1:** el alumno puede decir, en sus palabras, la diferencia entre "escribir la instrucción cada vez" y "guardarla como habilidad".

---

## Lección 2: Construye la tuya (15–20 min)

**Setup:** muéstrale que existe `modulo-3/starter/SKILL-plantilla.md` (una plantilla con espacios marcados `[AQUÍ VA...]`). Su trabajo: copiarla a `.claude/skills/secciones-de-sitio/SKILL.md` y completar los espacios.

**Guíalo pieza por pieza (una por respuesta):**

1. **`description`**: el disparador. Ayúdalo a escribir una descripción concreta: cuándo debe activarse (ejemplo real, no el de la plantilla: "usar cuando pida crear o actualizar una sección de mi sitio personal como proyectos, experiencia o habilidades"; nota para ti: aquí "habilidades" es la sección de su sitio, no la habilidad de Claude Code que está construyendo). Si la deja vaga ("para mi sitio"), señala el riesgo: una descripción vaga hace que Claude no sepa cuándo usarla, o la use quiere o no.
2. **Formato**: recupera lo que definió en el módulo 2 (largo, persona, estructura) y que lo traslade aquí, para que TODAS sus futuras secciones salgan consistentes.
3. **Tono y restricciones**: igual, recupera del módulo 2. Refuerza la regla de "solo hechos que estén en mis notas, nada inventado", ya la vio en el módulo 2, aquí se vuelve permanente.

**Crea el archivo real** en `.claude/skills/secciones-de-sitio/SKILL.md` con lo que el alumno definió (tú escribes el archivo; él dicta el contenido). Muéstraselo completo.

**Compuerta L2:** el archivo `.claude/skills/secciones-de-sitio/SKILL.md` existe, con una `description` concreta (no la plantilla sin completar) y las secciones de formato/tono llenas con las reglas del alumno.

---

## Lección 3: Pruébala en vivo (10–15 min)

**Concepto:** define en una frase por qué hace falta avisarle a Claude: *Claude revisa qué habilidades existen al empezar la conversación (o cuando le pides que revise de nuevo); si acabas de crear una, hace falta decírselo.*

**Antes de darle ninguna instrucción al alumno, registra el estado intermedio.** Actualiza `mi-trabajo/progreso.md` ahora mismo: "Módulo 3, en progreso: Lecciones 1-2 completas (`.claude/skills/secciones-de-sitio/SKILL.md` creado), pendiente Lección 3 (prueba en vivo)." Esto es lo que permite que la próxima sesión (reinicie o no) retome exactamente aquí en vez de repetir el módulo entero desde cero.

**Instrucción al alumno:** que escriba `/reload-skills`. Eso le dice a Claude que revise si hay habilidades nuevas o cambiadas en disco, sin salir de la sesión. Como esta es la primera habilidad que crea en todo el curso, es probable que `/reload-skills` diga "0 añadidas" (la carpeta `.claude/skills/` no existía todavía cuando arrancó esta sesión, así que Claude no la estaba vigilando). Si pasa eso, no es un error: dile que salga de Claude Code (escribiendo `exit` o cerrando la terminal) y lo abra de nuevo con `claude`, en la misma carpeta del curso. En habilidades futuras (como la del módulo 5) ya no hará falta reiniciar, `/reload-skills` sola alcanza.

**Nota para ti (el tutor):** si el alumno termina reiniciando, esta lección cruza el reinicio de sesión: tú no vas a "ver" lo que pasa después de que cierre. Cuando vuelva a abrir Claude Code (o en el siguiente mensaje, si `/reload-skills` funcionó sin reiniciar), esa respuesta debe: leer `mi-trabajo/progreso.md`, notar que está a mitad del módulo 3 en la Lección 3, y retomar aquí mismo pidiéndole la prueba en vivo, sin repetir las lecciones 1 y 2. **Ojo con un caso concreto:** si el alumno, apenas reabre, escribe directamente la frase de prueba (p. ej. "necesito la sección de proyectos de mi sitio") sin saludar primero, IGUAL lee `mi-trabajo/progreso.md` antes de dejar que la habilidad responda, y enmarca el resultado dentro del curso en la misma respuesta ("¡perfecto, esa era justo la prueba de esta lección, y tu habilidad se activó sola!"). Nunca dejes que la habilidad responda en silencio como si el curso no existiera.

**La prueba real:** pídele que escriba, en español normal y SIN mencionar la palabra "skill"/"habilidad" ni el nombre del archivo: `necesito la sección de proyectos de mi sitio`. Dale espacio para confirmar que su propia habilidad respondió, no tú.

**Verificación pedagógica:** si la habilidad se activó bien, señala el momento: *eso que acaba de pasar: pediste algo normal y se activó tu receta guardada sola, es toda la magia de una habilidad.* Repite el ejercicio para `experiencia` (puede pedirlo distinto: "ahora la de experiencia").

Genera ambos archivos con la habilidad: `mi-trabajo/secciones/proyectos.md` y `mi-trabajo/secciones/experiencia.md`, a partir de `quien-soy.md`.

**Esto se generaliza (dilo explícito):** *lo que acabas de construir no es solo para tu sitio: cualquier tarea que repites una y otra vez con el mismo formato es candidata a convertirse en una habilidad.* Dale 2–3 ejemplos concretos ajenos al curso: armar slides con el mismo patrón de diseño cada semana, resumir entrevistas de usuarios siempre con la misma estructura, convertir feedback de clientes en tickets con el mismo formato. Pregúntale: *¿se te ocurre una tarea tuya, de tu trabajo real, que repites así?* No hace falta que la construya hoy, solo que la nombre.

**Compuerta L3 (checklist):**
- [ ] `mi-trabajo/secciones/proyectos.md` existe, generado por la habilidad.
- [ ] `mi-trabajo/secciones/experiencia.md` existe, generado por la habilidad.
- [ ] El alumno confirmó que activó la habilidad con lenguaje natural, sin mencionar su nombre.
- [ ] El alumno nombró una tarea repetitiva de su propio trabajo (fuera del curso) que podría convertir en una habilidad.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L3.
2. Actualiza `mi-trabajo/progreso.md`: módulo 3 completado, fecha, artefactos (`SKILL.md`, `secciones/proyectos.md`, `secciones/experiencia.md`).
3. Recapitula en 3 líneas: una habilidad es una receta guardada; la `description` es el disparador; se activa sola con lenguaje natural.
4. Anticipa el módulo 4 en una frase: *una habilidad sigue una receta tuya, un agente además puede decidir por su cuenta. Y ahí vuelve la ventana de contexto que mencionamos en el módulo 2.* Sin más detalle.
5. Cierra: `👉 escribe: /modulo-4` (o `/continuar` para parar aquí).

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| Faltan `quien-soy.md` o `sobre-mi.md` | Saltó módulos anteriores | Dirige a `/modulo-1` o `/modulo-2` según cuál falte |
| `/reload-skills` dice "0 añadidas" | Esperado la primera vez: la carpeta `.claude/skills/` no existía cuando arrancó la sesión | Normal, no es un error. Pide que reinicie de verdad (exit y volver a abrir `claude`) |
| La habilidad sigue sin activarse después de reiniciar | No reinició de verdad, o la `description` quedó vaga | Primero confirma que sí cerró y volvió a abrir `claude`; si sí, revisa la `description` juntos, hazla más específica |
| Escribió el nombre de la habilidad o "usa mi skill" en la prueba | Quiso "ayudar" a que funcione | Explica que el punto es que NO haga falta nombrarla; pide que lo intente de nuevo en lenguaje totalmente natural |
| No sabe dónde está `.claude/skills/` | Carpeta oculta, confusión de rutas | Tú creas y confirmas la ruta completa; no requiere que la navegue a mano |
| La habilidad genera contenido inventado | Reglas de tono/formato no incluyeron la restricción de "solo hechos reales" | Edita el `SKILL.md` juntos para añadirla explícitamente |
| Cerró la terminal sin querer antes de tiempo | Confusión sobre cuándo cerrar | Si ya registraste el progreso intermedio de la Lección 3, `/continuar` retoma justo donde estaba, sin perder nada |
