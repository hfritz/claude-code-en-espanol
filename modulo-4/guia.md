# Guía interna — Módulo 4: Agentes y subagentes

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno tiene: un subagente propio (`armador-de-contenido`) que arma el paquete de contenido de su sitio, y entiende dos conceptos clave: (a) la anatomía de un agente (cerebro, objetivo, herramientas, memoria) y (b) la **ventana de contexto** — sembrada en el módulo 2, enseñada aquí de verdad porque es LA razón por la que existen los subagentes: cada uno arranca con su propia ventana fresca, y por eso dividir el trabajo funciona mejor que un solo agente que lo carga todo.

**Prerrequisito:** `mi-trabajo/secciones/proyectos.md` y `mi-trabajo/secciones/experiencia.md` (módulo 3), además de `quien-soy.md` y `sobre-mi.md`. Verifícalos antes de empezar; si faltan, dirige al módulo correspondiente.

---

## Lección 1 — Qué es un agente (10–15 min)

**Concepto:** recupera la skill del módulo 3 como punto de comparación. Una skill es una receta que **tú mismo** (el Claude de esta conversación) sigues cuando aplica. Un **agente** es distinto: define en una frase — *un agente es un Claude configurado con su propio trabajo, que puede tomar decisiones dentro de ese trabajo en vez de solo seguir una receta fija.* Un **subagente** es un agente al que la conversación principal le delega una tarea y que trabaja por su cuenta, aparte, y vuelve con un resultado.

**Anatomía en cuatro piezas — una por respuesta, con micro-ejemplo cada vez:**

1. **Cerebro** — cómo piensa y qué personalidad de trabajo tiene. Ejemplo: "eres un editor cuidadoso que organiza, no inventa."
2. **Objetivo** — qué debe lograr, concreto y verificable. Ejemplo: "producir un archivo con todo el contenido del sitio, listo para publicar."
3. **Herramientas** — qué puede hacer (leer archivos, escribir archivos, buscar en la web...) y qué NO puede hacer. Ejemplo: "puede leer y escribir archivos; no navega internet."
4. **Memoria** — qué información tiene disponible y qué NO recuerda entre llamadas. Ejemplo: "lee tus notas cada vez que lo llamas; no recuerda conversaciones pasadas."

**Compuerta L1:** el alumno puede nombrar las cuatro piezas y explicar, en sus palabras, la diferencia entre una skill y un agente.

---

## Lección 2 — La ventana de contexto (15–20 min)

**Retoma la semilla del módulo 2:** *dijimos que Claude tiene un límite de memoria de trabajo — ahora vemos qué significa de verdad y por qué te importa.*

**Concepto, en capas (una capa por respuesta):**

1. **Qué es:** define **ventana de contexto** en una frase — *todo lo que Claude puede "tener presente" en una conversación a la vez: tus instrucciones, los archivos que ha leído, todo lo que han hablado.* Analogía: una mesa de trabajo — caben tantos papeles a la vez; si sigues apilando, algo tiene que ceder.
2. **Qué pasa cuando se llena:** en una conversación muy larga, con muchos archivos leídos, la ventana se llena. Claude puede perder detalle de lo que pasó al principio, o resumir (compactar) para seguir cabiendo. No es que "se vuelva tonto" — es que la mesa tiene un tamaño.
3. **La solución — subagentes:** aquí está el porqué que estabas esperando. *Cuando delegas una tarea a un subagente, ese subagente arranca con SU PROPIA mesa vacía — no carga con todo lo que ha pasado en tu conversación principal. Se enfoca solo en su tarea, y cuando termina, solo su RESULTADO final vuelve a tu conversación — no todo el trabajo intermedio que hizo para llegar ahí.* Por eso dividir el trabajo en piezas más chicas, cada una en su propio subagente, funciona mejor que pedirle todo a un solo agente que tiene que cargar con absolutamente todo a la vez.

**Ejemplo concreto para anclarlo:** si le pides a un solo Claude que lea 10 archivos largos, escriba 5 secciones, y además siga charlando contigo del resto del curso, todo eso compite por el mismo espacio. Si en cambio le delegas "arma el contenido de mi sitio" a un subagente aparte, ese subagente usa SU espacio solo para eso — y tu conversación principal se queda liviana.

**Compuerta L2:** el alumno explica, en sus palabras, por qué un subagente con ventana propia ayuda comparado con un solo agente que lo hace todo. No exijas precisión técnica — la idea de "mesa propia, más espacio libre" es suficiente.

---

## Lección 3 — Construye tu subagente (15–20 min)

**Setup:** muéstrale `modulo-4/starter/agente-plantilla.md` — misma mecánica que la plantilla de skill del módulo 3, pero ahora con las cuatro piezas de la anatomía como secciones marcadas `[AQUÍ VA...]`.

**Guíalo pieza por pieza, recuperando la Lección 1:**

1. **`description`** (el disparador, igual que en skills): cuándo debe delegarse trabajo aquí. Ejemplo a afinar con el alumno: "usar cuando pida armar o actualizar el paquete completo de contenido de su sitio."
2. **Cerebro**: que decida la personalidad de trabajo — sugiere "editor cuidadoso que organiza, no inventa" si no se le ocurre nada.
3. **Objetivo**: un archivo único y concreto — `mi-trabajo/paquete-de-contenido.md` con todas las secciones listas.
4. **Herramientas**: ya viene fijado en la plantilla (`Read, Write`) — explica en una frase por qué: *solo necesita leer tus notas y escribir el resultado; no necesita nada más.*
5. **Memoria**: qué archivos debe leer — `quien-soy.md`, `sobre-mi.md`, todo en `secciones/`. Refuerza: *no recuerda conversaciones pasadas — cada vez que lo llames, relee estos archivos desde cero.*

**Crea el archivo real** en `.claude/agents/armador-de-contenido.md` con lo que el alumno definió.

**Prueba real:** pídele que le delegue la tarea en lenguaje natural, por ejemplo: `arma el paquete de contenido completo de mi sitio`. Cuando el subagente responda, señala el momento pedagógico: *eso que acaba de pasar — otro "Claude" trabajó aparte, con su propia ventana, y te devolvió solo el resultado — es un subagente en acción.*

**Compuerta L3 (checklist):**
- [ ] `.claude/agents/armador-de-contenido.md` existe con las cuatro piezas completas (no la plantilla sin llenar).
- [ ] `mi-trabajo/paquete-de-contenido.md` existe, generado por el subagente, con las secciones organizadas.
- [ ] El alumno confirmó que reconoció la delegación (otro Claude trabajó la tarea y volvió con el resultado).

---

## Extra opcional — Conecta una herramienta real (MCP)

**Concepto:** en una frase — *MCP (Model Context Protocol) es la forma en que Claude se conecta a servicios reales — tu correo, tu calendario, bases de datos — para que un agente los use como herramienta, sin que tengas que programar la conexión.*

Retoma la pieza "Herramientas" de la Lección 1: hoy tu subagente solo tiene Read y Write (archivos). En el mundo real, las herramientas de un agente pueden ser mucho más amplias — MCP es el mecanismo que lo permite.

**Si el alumno quiere probarlo (totalmente opcional — no bloquea el módulo, no pide nada si no le interesa):**
1. Fuera de Claude Code, en claude.ai, ve a Configuración → Conectores.
2. Conecta Gmail (o cualquier otro servicio que ya use — Calendar, Drive).
3. Vuelve a esta conversación y escribe `/mcp` para confirmar que la conexión está activa.
4. Pruébalo con algo simple: "¿tengo correos importantes sin leer hoy?" o "resume mi bandeja de entrada."

**Nota para ti (el tutor):** esto es un extra, no una lección con compuerta. Si el alumno no tiene Gmail, no le interesa, no puede autenticar, o el conector falla — no insistas, sigue directo al cierre del módulo. El objetivo es solo que sepa que MCP existe y cómo se llama; no es requisito para nada de lo que viene después en el curso.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L3.
2. Actualiza `mi-trabajo/progreso.md`: módulo 4 completado, fecha, artefactos (`armador-de-contenido.md`, `paquete-de-contenido.md`).
3. Recapitula en 3 líneas: anatomía de un agente (cerebro, objetivo, herramientas, memoria); la ventana de contexto tiene límite; los subagentes existen para no cargar todo en una sola ventana.
4. Anticipa el módulo 5 en una frase: *Ahora tuviste UN subagente. ¿Qué pasa si tienes varios trabajando a la vez, y alguien coordina el resultado? Eso es orquestación.* Sin más detalle.
5. Cierra: `👉 escribe: /modulo-5` (o `/continuar` para parar aquí).

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| Faltan secciones del módulo 3 | Saltó el módulo 3 o borró archivos | Dirige a `/modulo-3` |
| Confunde skill con agente | Conceptos parecidos | Repite el contraste: skill = receta que sigues tú mismo; agente/subagente = otro Claude que hace el trabajo aparte y vuelve con un resultado |
| No entiende para qué sirve la ventana de contexto | Concepto abstracto sin ejemplo propio | Usa el ejemplo concreto de la lección 2 (10 archivos + charla vs. delegar a un subagente aparte) |
| El subagente no se activa | `description` vaga, o no delegó explícitamente | Revisa la `description` juntos; pídele que sea más directo en la petición ("arma el paquete de contenido de mi sitio") |
| El subagente inventa contenido que no está en las notas | Cerebro/objetivo no reforzó "organizar, no inventar" | Edita `armador-de-contenido.md` para reforzar la restricción |
| Pregunta si el subagente "es otra IA distinta" | Curiosidad legítima | Aclara: es el mismo Claude, pero arrancado con instrucciones propias y una ventana de contexto vacía — no es "otra empresa" ni "otro modelo" necesariamente, es una instancia separada con su propio enfoque |
| El conector de Gmail no conecta / no tiene cuenta de Google | Es un extra opcional, no todos lo tendrán listo | Recuérdale que es 100% opcional — no bloquea nada. Sigue directo al cierre del módulo |
