# Guía interna — Módulo 5: Orquestación

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno tiene: `mi-trabajo/paquete-de-contenido-final.md` — producido por un equipo de tres subagentes especializados que trabajaron en paralelo y una skill de corrección universal aplicada al final. Entiende qué significa "orquestación" de verdad: coordinar varios trabajadores, algunos al mismo tiempo, y juntar sus resultados — y que un buen flujo de trabajo usa la herramienta correcta para cada paso, no "más subagentes = más sofisticado".

**Prerrequisito:** `.claude/agents/armador-de-contenido.md` y `mi-trabajo/paquete-de-contenido.md` (módulo 4). Verifícalos antes de empezar; si faltan, dirige a `/modulo-4`.

---

## Lección 1 — Qué es la orquestación, de verdad (10 min)

**Concepto:** define **orquestación** en una frase — *coordinar a varios trabajadores (subagentes) para que hagan partes distintas de un trabajo, algunos al mismo tiempo, y juntar sus resultados en uno solo.* (Nota para ti: esto es lo que en inglés a veces se llama "workflow" — no hace falta usar esa palabra con el alumno, pero si la usa, confirma que es lo mismo.)

**Contraste con el módulo 4:** en el módulo 4 tuviste UN subagente (`armador-de-contenido`) que hizo todo: leyó, organizó, detectó huecos. Funcionó, pero cargó con tres trabajos distintos a la vez. Pregúntale: *¿qué pasaría si en vez de uno, tuvieras tres especialistas — cada uno mirando algo distinto en los mismos archivos — trabajando los tres a la vez?*

**La pieza nueva: "al mismo tiempo".** Ya sabe (módulo 4) que un subagente tiene su propia ventana de contexto. Lo nuevo hoy: puedes despachar varios subagentes **en paralelo** — no uno, esperar, luego el siguiente — sino los tres a la vez, y el resultado de todos vuelve junto. Eso es más rápido y, cuando cada uno mira algo distinto, más claro que pedirle todo a uno solo.

**Compuerta L1:** el alumno explica, en sus palabras, la diferencia entre "un subagente hace todo" (módulo 4) y "varios especialistas trabajan a la vez, cada uno en lo suyo" (hoy).

---

## Lección 2 — Arma tu equipo de especialistas (15–20 min)

**Setup:** muestra `modulo-5/starter/especialista-plantilla.md`. Ya conoce la anatomía completa (cerebro, objetivo, herramientas, memoria) del módulo 4 — esta vez va más rápido, y tú guías menos paso a paso porque ya lo sabe hacer.

Cada uno de los tres mira el mismo material con un lente distinto — es la misma idea que pedirle a un par, a tu manager, y a alguien que te reporta que revisen lo mismo: cada quien nota algo diferente.

**Los tres roles (defínelos, uno por respuesta, antes de que el alumno los construya):**

1. **`especialista-de-contenido`** — organiza el material en secciones. El alumno puede prácticamente reusar/adaptar su `armador-de-contenido` del módulo 4 con este nuevo nombre.
2. **`especialista-de-tono`** — objetivo concreto: leer todo el texto y compararlo contra la voz de `sobre-mi.md`, señalando frases que no suenan al alumno.
3. **`especialista-de-huecos`** — objetivo concreto: tomar los "Pendientes" vagos del módulo 4 y convertirlos en preguntas concretas y respondibles (ejemplo: de "faltan fechas" a "¿en qué año hiciste el proyecto de la cafetería?").

**Deja que el alumno decida cerebro/objetivo de cada uno con tus ejemplos como ancla** — no se los dictes palabra por palabra; es su equipo. Confirma con él por qué los tres pueden trabajar a la vez: *leen los mismos archivos, pero cada uno busca algo distinto — no dependen del resultado del otro.*

**Crea los tres archivos reales**: `.claude/agents/especialista-de-contenido.md`, `.claude/agents/especialista-de-tono.md`, `.claude/agents/especialista-de-huecos.md`.

**Compuerta L2:** los tres archivos existen, cada uno con una `description` que distingue claramente su trabajo del de los otros dos (no descripciones idénticas o intercambiables).

---

## Lección 3 — Despacha en paralelo y observa (10–15 min)

**La prueba real:** pide al alumno que despache a los tres especialistas de una sola vez, con una petición que abarque el trabajo completo — por ejemplo: `dile a mi equipo de especialistas que revisen el contenido completo de mi sitio: organización, tono y huecos`. Como Claude decide cuándo delegar según las `description`, una petición que toque los tres frentes debería activar a los tres.

**Momento pedagógico (señálalo cuando vuelvan los tres resultados):** *fíjate — no esperaste a que uno terminara para que empezara el siguiente. Los tres trabajaron a la vez, cada uno con su propia ventana, y ahora tienes los tres resultados juntos. Eso es orquestar.*

**Esto se generaliza (el corazón de la lección):** *esto que acabas de hacer — pedirle a tres lentes distintos que miren lo mismo, a la vez — es exactamente lo mismo que pedirle a un par, a tu manager, y a alguien que te reporta que revisen un documento antes de mandarlo. La diferencia es que normalmente esperas días juntando esas tres opiniones por separado; aquí las tuviste en minutos, en paralelo.* Pregúntale: *¿en qué situación real de tu trabajo te serviría pedir tres lentes distintos así, en paralelo?* Dale espacio para que lo nombre — no hace falta que lo construya hoy.

**Si Claude los despachó uno por uno en vez de a la vez:** no es un error del alumno — puede pasar según cómo esté formulada la petición. Sugiere reformular pidiendo explícitamente las tres cosas juntas en una sola frase, en vez de tres peticiones separadas.

**Síntesis:** pide que la conversación principal junte los tres resultados en un solo archivo: `mi-trabajo/paquete-de-contenido-borrador.md` — contenido organizado + tono corregido + huecos convertidos en preguntas (que el alumno responda las que pueda, ahí mismo).

**Compuerta L3 (checklist):**
- [ ] `mi-trabajo/paquete-de-contenido-borrador.md` existe, con aportes reconocibles de los tres especialistas.
- [ ] El alumno respondió al menos una de las preguntas de huecos.
- [ ] El alumno nombró una situación real de su trabajo donde le serviría pedir varios lentes en paralelo (ej. par + manager + reporte).

---

## Lección 4 — El corrector universal (10–15 min)

**Setup:** antes de construir nada, ancla el punto central de la lección: *todo lo que hemos construido hoy — los tres especialistas — solo sabe de sitios personales. Esta última pieza es distinta: no sabe nada de sitios. Solo sabe de texto.*

**Construye la skill** (no un subagente — recupera el concepto del módulo 3) a partir de `modulo-5/starter/corrector-de-texto-plantilla.md`: ortografía, gramática, claridad. Deja claro qué NO hace (no cambia el tono — eso ya lo hizo el especialista de tono; no inventa contenido).

**El ejemplo que hace universal el concepto — dilo explícitamente:** *esta misma skill, tal cual la acabas de construir, sirve para revisar un post de LinkedIn antes de publicarlo, un correo importante, o el informe que entregas el lunes. No tiene que ver con tu sitio — tiene que ver con cualquier texto que escribas de aquí en adelante.* Si el alumno tiene a mano algo real que haya escrito fuera del curso (un mensaje, un post), invítalo a probarlo ahí mismo — no obligatorio, pero si lo hace, es la prueba viva de la universalidad.

**Aplícala:** que la use sobre `paquete-de-contenido-borrador.md`. Guarda el resultado final en `mi-trabajo/paquete-de-contenido-final.md`.

**Compuerta L4 (checklist):**
- [ ] `.claude/skills/corrector-de-texto/SKILL.md` existe.
- [ ] `mi-trabajo/paquete-de-contenido-final.md` existe, con el contenido corregido.
- [ ] El alumno puede decir, en sus palabras, un uso de esta skill que NO tenga que ver con su sitio.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L4.
2. Actualiza `mi-trabajo/progreso.md`: módulo 5 completado, fecha, artefactos (los tres especialistas, la skill, `paquete-de-contenido-final.md`).
3. Recapitula en 3 líneas: orquestar es coordinar varios trabajadores, algunos a la vez, y juntar resultados; usaste tres subagentes en paralelo más una skill universal; el paquete final de tu sitio ya está listo.
4. Anticipa el módulo 6 en una frase: *todo lo que has construido — desde `quien-soy.md` hasta este paquete final — está a un paso de ser un sitio de verdad, en internet, con tu URL.* Sin más detalle técnico (no menciones Vercel ni HTML todavía).
5. Cierra: `👉 escribe: /modulo-6` (o `/continuar` para parar aquí).

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| Faltan `armador-de-contenido.md` o `paquete-de-contenido.md` | Saltó el módulo 4 | Dirige a `/modulo-4` |
| Los tres especialistas quedan casi idénticos | No diferenció bien objetivo/cerebro de cada uno | Vuelve a la Lección 2, pide una frase que distinga a cada uno del resto |
| Los especialistas no se despachan a la vez | Petición formulada como tres pedidos separados | Sugiere una sola frase que mencione los tres frentes de trabajo |
| Confunde el corrector con el especialista de tono | Se parecen (ambos "arreglan texto") | Aclara la frontera: tono = que suene a ti (subagente, mira tu voz particular); corrector = ortografía/gramática/claridad (skill, no sabe nada de tu voz) |
| No se le ocurre un uso del corrector fuera del sitio | Falta de ejemplo concreto | Sugiere: "pruébalo con un mensaje que tengas que mandar hoy" |
| Quiere que el corrector también arregle el tono | Malentendido de su alcance | Recuerda: "Qué NO hace" en su propio archivo — edítenlo juntos si hace falta reforzarlo |
