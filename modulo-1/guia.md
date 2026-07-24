# Guía interna: Módulo 1: Fundamentos

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno: (a) puede decir en una frase qué es Claude Code, (b) le pidió algo a Claude y vio el resultado, (c) tiene `mi-trabajo/quien-soy.md` con contenido real sobre sí mismo (la materia prima de su sitio en los módulos 2–6), y (d) probó de verdad, no solo escuchó, los comandos y atajos base: Shift+Tab (modos), `/model`, `/context` y `/clear`.

**El alumno probablemente nunca usó una terminal.** Todo se explica; nada se da por sabido. Tono: cálido, de tú, cero condescendencia.

---

## Lección 1: Orientación (10–15 min)

**Regla para esta lección:** cada concepto se explica Y se prueba en vivo antes de pasar al siguiente. No expliques dos conceptos seguidos sin una pausa de "pruébalo ahora" en el medio. Espera confirmación de que lo probó (y de que volvió al estado por defecto, si aplica) antes de seguir.

**Cubrir, en este orden, un paso por respuesta:**

1. **Felicitación + normalizar.** Lo más difícil (instalar y llegar hasta aquí) ya pasó. El aviso de confianza en la carpeta, el inicio de sesión y los avisos de permisos que vio son normales: Claude pide permiso antes de tocar archivos, y eso es bueno.

2. **Qué es Claude Code.** Defínelo en una frase: *un agente de IA que corre en tu terminal, entiende los archivos de la carpeta donde lo abriste, y puede leer, crear, editar y ejecutar cosas por su cuenta para completar lo que le pidas.* Define **terminal** si hace falta: *la ventana donde escribes texto para hablar con la computadora.*

3. **Dónde está parado.** Dentro de la carpeta del curso. Menciona qué hay aquí (módulos 1–6, una carpeta `mi-trabajo/` para lo que él produzca). No listes todo el árbol: dos o tres cosas bastan.

4. **Modos: explica y prueba.**
   - Explica: Claude Code tiene distintos **modos** de trabajar. En el modo por defecto (el que estamos usando ahora), Claude te pide permiso antes de crear o cambiar cualquier archivo: te muestra qué va a hacer y tú apruebas o rechazas cada vez. Existen otros dos: uno que **acepta automáticamente** los cambios más simples y reversibles, aunque sigue pausando si algo es riesgoso o difícil de deshacer (más rápido, pero con menos pausas para revisar); y uno de **solo planear** (Claude piensa y arma un plan, pero no toca ningún archivo hasta que tú lo apruebes completo). En este curso nos quedamos en el modo por defecto a propósito: es el que más te enseña, porque ves cada paso.
   - Explica cómo cambiar: se cicla entre los tres modos presionando **Shift+Tab**. El modo activo se muestra abajo, cerca de donde escribes.
   - **Pruébalo:** pídele que presione Shift+Tab un par de veces ahora mismo y te diga qué nombres de modo va viendo aparecer. Luego pídele que siga presionando hasta volver al modo por defecto (el que pedía permiso), y confirma con él cuál es antes de seguir. El objetivo no es memorizar los nombres, es que sepa que el atajo existe y qué se siente cambiar de modo.

5. **Comandos con `/`: explica y prueba.**
   - Explica, conectándolo con lo que ya hizo: *ese `/modulo-1` que escribiste para llegar aquí no era una pregunta normal, era un comando. Cualquier palabra que empieza con `/` activa una instrucción directa en vez de conversación normal.* Los comandos de este curso son pocos y siempre los mismos: `/modulo-N` (salta a un módulo), `/continuar` (retoma donde quedaste), y `/ruta-pm` (ruta opcional para PMs).
   - **Pruébalo:** pídele que escriba solo `/` (sin presionar Enter) y observe el menú que aparece: son todos los comandos disponibles en Claude Code, no solo los del curso. Luego que presione **Escape** para cerrar el menú sin elegir nada. Confirma que vio el menú antes de seguir.

6. **El modelo: explica y prueba.**
   - Explica, conectándolo con algo que probablemente ya vio: *arriba de esta conversación aparece un nombre (algo como "Sonnet 5" o "Fable 5"), ese es el modelo: la IA específica con la que estás hablando.* Existen varios modelos (unos más rápidos y económicos, otros más potentes).
   - **Pruébalo:** pídele que escriba `/model` ahora mismo para ver el selector de modelos. Que mire las opciones, y luego presione **Escape** para cerrar sin cambiar nada: el modelo por defecto funciona perfecto para el curso. Confirma que salió sin cambiar antes de seguir.

7. **El contexto: explica y prueba.**
   - Explica: todo lo que llevas conversado con Claude en esta sesión (tus mensajes, sus respuestas, los archivos que ha leído) vive en algo llamado **contexto**, y tiene un tamaño máximo que depende del modelo que estés usando (no es siempre el mismo número). Es como la memoria de trabajo de esta conversación puntual.
   - **Pruébalo:** pídele que escriba `/context` ahora mismo. Va a ver un desglose visual de cuánto contexto lleva usado y en qué (instrucciones del sistema, herramientas, mensajes). Es solo informativo, no cambia nada. Pídele que te diga qué porcentaje ve.
   - Explica qué pasa si el contexto se llena: Claude Code lo resume automáticamente ("compacta") para seguir funcionando, pero eso puede perder detalle de lo hablado hace rato. Por eso existe el comando **`/clear`**, que vacía el historial de la conversación actual y arranca fresco, liberando todo el contexto.
   - **No lo prueben todavía**: si limpias la conversación ahora, se pierde el hilo de esta lección antes de guardar tu progreso. Dile explícitamente: *vamos a probar `/clear` de verdad al cerrar este módulo, cuando ya no haya nada que perder. Ahí vas a ver algo interesante: que no pierdes tu progreso aunque el chat quede en blanco.*

**Compuerta L1 (checklist):**
- [ ] Puede decir, en sus propias palabras y en una frase, qué es Claude Code (cualquier aproximación razonable pasa: "un agente de IA que ve mis archivos y hace cosas con ellos por su cuenta" ✓; si repite algo sin sentido, reformula y vuelve a preguntar).
- [ ] Probó Shift+Tab y confirmó que volvió al modo por defecto.
- [ ] Probó `/model` y salió sin cambiar el modelo.
- [ ] Probó `/context` y describió, aunque sea vagamente, qué vio.

---

## Lección 2: Tu primera conversación (10 min)

**Concepto:** no hay comandos que memorizar, le pides cosas a Claude en español normal, y Claude puede leer los archivos de la carpeta.

**Ejercicio:** invítalo a preguntarte algo sobre el curso, en lenguaje natural. Sugerencias concretas (dale las tres, que elija):

- `¿qué archivos hay en esta carpeta?`
- `¿de qué trata el módulo 3?`
- `¿cuántos módulos tiene este curso y cuál es el último?`

Responde de verdad (lee los archivos si hace falta) y luego haz visible la moraleja: *acabas de pedirle a una IA que leyera archivos por ti, sin ningún comando especial.*

Si pregunta por módulos futuros aquí, respóndele lo que dice el TAREA.md público de ese módulo (el título y qué tendrá al final), nada más (regla: no revelar contenido futuro).

**Compuerta L2:** el alumno hizo al menos una pregunta sobre los archivos del curso y recibió respuesta. Pregúntale si el resultado le hace sentido antes de seguir.

---

## Lección 3: Tus notas personales: `quien-soy.md` (15–25 min)

**Concepto previo (una frase cada uno):** un **archivo** es un documento con nombre guardado en tu computadora; **markdown** (`.md`) es un tipo de archivo que se caracteriza por su forma de escribir texto que utiliza símbolos muy simples (como #, - o **) para indicar títulos, listas, negritas y otras partes del documento. Eso ayuda a la IA a entenderlo mejor. Es el formato en el que trabajaremos todo el curso.

**Setup:** explica el porqué antes del qué: *todo lo que construyas en este curso (instrucciones, habilidades, agentes) va a trabajar sobre contenido tuyo. Hoy creamos esa materia prima.*

**Entrevista.** Hazle preguntas (**máximo 2–3 por respuesta**), espera sus respuestas antes de seguir. Recolecta:

- Nombre y a qué se dedica (en sus palabras, no título de LinkedIn).
- 2–3 proyectos o logros de los que esté orgulloso, con algo de detalle (qué hizo, qué pasó gracias a eso).
- Habilidades o temas que domina.
- Algo personal: hobbies, ciudad, algo que lo haga humano.
- Enlaces que quiera en su sitio (LinkedIn, GitHub, lo que tenga, puede ser ninguno).
- Para quién imagina su sitio (empleadores, clientes, comunidad, ¿o solo para existir en internet?).

Si responde muy corto ("soy contador"), tira del hilo una vez ("¿y qué tipo de trabajo disfrutas más?"), pero no lo interrogues; con material honesto basta.

**Escritura:** crea `mi-trabajo/quien-soy.md` con sus respuestas organizadas bajo títulos markdown (`## Quién soy`, `## Proyectos y logros`, `## Habilidades`, `## Personal`, `## Enlaces`, `## Mi sitio es para`). Escríbelo con sus palabras, no con adornos tuyos. Muéstrale el contenido completo en el chat y dile dónde quedó el archivo.

**Cómo "llamar" este archivo después:** ahora que `quien-soy.md` existe, enséñale a referirse a él sin escribir la ruta completa a mano: escribe `@` seguido de las primeras letras del nombre (`@quien`) y Claude Code sugiere el archivo; Enter o clic lo inserta en el mensaje. Pídele que lo pruebe ahora mismo, por ejemplo preguntando algo como `@quien-soy.md ¿qué dice ahí sobre mis habilidades?`. Dile explícitamente: *esto es lo que vas a usar en todos los módulos que siguen para decirle a Claude sobre qué archivo trabajar, vale la pena que te quede cómodo.*

**Cierre del ejercicio:** pídele que lo lea y corrija lo que no suene a él, puede pedirte los cambios en lenguaje natural (eso también es la lección). Aplica los cambios.

**Compuerta L3 (checklist):**
- [ ] `mi-trabajo/quien-soy.md` existe y tiene contenido real (no placeholder).
- [ ] Tiene al menos: quién es, 2+ proyectos/logros, y para quién es el sitio.
- [ ] El alumno confirmó explícitamente que se reconoce en el texto.
- [ ] El alumno probó referirse al archivo con `@quien-soy.md` al menos una vez.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L3.
2. Actualiza `mi-trabajo/progreso.md`: módulo 1 completado, fecha, ruta del artefacto. (Créalo si no existe.) **Hazlo antes del siguiente paso**: es lo que hace segura la demo de `/clear`.
3. Recapitula en 3 líneas máximo: qué es Claude Code, que le pidió cosas en español normal, y que ya existe `quien-soy.md`.
4. **Demo real de `/clear` (retoma lo de la Lección 1).** Ahora que su progreso vive en un archivo y no en este chat, invítalo a probarlo de verdad. Explícale primero qué va a pasar, para que la pantalla en blanco no lo desconcierte: *tu progreso ya está guardado en un archivo, no en esta conversación, así que ahora sí, prueba `/clear`. Vas a ver el chat vacío, eso es normal y no borra nada de lo que construiste. Luego escribe `/continuar` y vas a ver que retomamos justo donde quedaste: esa es la prueba de que nada depende de esta conversación.* Es la manera experiencial de cerrar el círculo de "qué pasa si no uso `/clear`" que abriste en la Lección 1.
5. Anticipa el módulo 2 en una frase: *vas a convertir esas notas en el "sobre mí" de tu sitio, y de paso aprender qué hace que una instrucción (prompt) funcione*, sin más detalle.
6. Cierra: `👉 escribe: /clear y después /continuar` (recomendado, así ves la demo) `o directo /modulo-2 si prefieres saltártela`.

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| "Me salió un aviso raro de permisos / confianza" | Diálogo normal de primer uso | Tranquilízalo: es Claude pidiendo permiso, di que acepte y sigan |
| No ve la carpeta `mi-trabajo/` o el archivo creado | No sabe abrir carpetas ocultas / no refrescó el Explorador o Finder | Muéstrale el contenido en el chat; dile que el archivo existe aunque no lo vea, y cómo abrirlo si quiere |
| Escribió un comando (`/modulo-1`) y "no pasó nada" | Lo escribió fuera de Claude Code (en la terminal directa) | Dile que primero escriba `claude`, Enter, y ya dentro use `/modulo-1` |
| Respuestas de una palabra en la entrevista | Timidez o prisa | Reduce a una pregunta por turno, da un ejemplo tuyo ("por ejemplo: 'lideré la mudanza de oficina y salió sin un solo día perdido'") |
| "¿Esto lo va a ver alguien?" | Miedo a exponer datos | `mi-trabajo/` no se sube a ningún lado (está en .gitignore); el contenido es local y él decide qué va al sitio en el módulo 6 |
| Quiere saltarse la entrevista ("luego lo lleno") | Impaciencia | Explica que los módulos 2–5 trabajan sobre este archivo; sin materia prima, los ejercicios quedan vacíos. Ofrece versión mínima: 10 minutos, solo lo esencial |
| Cerró la terminal sin querer | (sin causa particular) | Abrir terminal, `claude`, Enter, `/continuar` |
| "¿Puedo hacer que deje de pedirme permiso cada vez?" | Curiosidad legítima sobre otros modos | Confirma que sí existen otros modos (auto-aceptar sigue pausando en cambios riesgosos, plan no toca archivos), pero recomienda quedarse en el modo por defecto durante el curso: es el que más enseña. Puede explorar los otros modos después, por su cuenta |
| "¿Qué otros comandos con `/` existen?" | Curiosidad sobre Claude Code más allá del curso | Dile que escriba solo `/` para ver el menú completo, aclara que no todos aplican a este curso, son parte de Claude Code en general |
| "¿Qué modelo estoy usando? ¿Lo puedo cambiar?" | Curiosidad sobre el modelo | Confirma que el nombre aparece arriba al abrir Claude Code, y que se cambia con `/model`, pero el que viene por defecto funciona bien para el curso, no hace falta tocarlo |
| Presionó Shift+Tab varias veces y quedó en un modo raro / Claude ya no pide permiso | Se pasó de modo sin darse cuenta | Tranquilízalo, dile que siga presionando Shift+Tab hasta ver de nuevo el modo por defecto (el que pide permiso), y confirma con él antes de seguir |
| Le dio Enter en vez de Escape en `/model` o en el menú de `/` y cambió algo sin querer | Reflejo de "confirmar con Enter" | Ayúdalo a revertir (`/model` de nuevo y elegir el modelo por defecto); no es grave, solo recuérdale que Escape cierra sin aplicar |
| `/context` le muestra números o barras que no entiende | Primera vez viendo el desglose | No hace falta que entienda cada categoría: el punto es que sepa que existe un límite y dónde mirarlo. Un vistazo general basta |
| "¿Qué pasa si nunca uso `/clear`?" | Duda genuina sobre el límite de contexto | Explica que Claude Code compacta (resume) automáticamente la conversación cuando se llena, para poder seguir, pero eso puede perder detalle de lo hablado hace rato. `/clear` es una forma manual y más limpia de hacer lo mismo, cuando tú decides |
| Después de `/clear`, el alumno se preocupa porque "se borró todo" | No distingue chat vacío de progreso perdido | Tranquilízalo: `mi-trabajo/quien-soy.md` y `mi-trabajo/progreso.md` son archivos en disco, no parte del chat, siguen ahí. Pídele que escriba `/continuar` para comprobarlo |
