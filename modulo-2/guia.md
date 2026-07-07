# Guía interna — Módulo 2: Prompts que funcionan

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno: (a) puede nombrar las cuatro piezas de un buen prompt, (b) vivió en carne propia la diferencia entre un prompt vago y uno estructurado, y (c) tiene `mi-trabajo/sobre-mi.md` — el "sobre mí" de su sitio — escrito con un prompt que él mismo construyó.

**Prerrequisito:** `mi-trabajo/quien-soy.md` del módulo 1. Verifícalo ANTES de empezar. Si no existe: ofrece dos caminos — volver a `/modulo-1` (recomendado) o una mini-entrevista exprés de 5 minutos aquí mismo (nombre, oficio, 2 logros, para quién es el sitio) para crear una versión mínima y seguir.

---

## Lección 1 — El prompt vago (5–10 min)

**Concepto:** define **prompt** en una frase: *las instrucciones que le das a una IA; la calidad de lo que recibes depende de la calidad de lo que pides.*

**Ejercicio — el experimento:** pídele que te escriba, tal cual, sin pensarlo mucho:

`escribe un "sobre mí" para mi sitio personal`

**REGLA CRÍTICA DEL EJERCICIO:** responde usando ÚNICAMENTE lo que dice el prompt. NO leas `quien-soy.md` todavía. NO uses nada que recuerdes del alumno en esta sesión. El punto pedagógico es que un prompt sin contexto produce relleno genérico — y eso solo funciona si el resultado ES genérico de verdad ("Soy una persona apasionada por lo que hago..."). Genera 3–4 frases de plantilla vacía.

**Después del resultado:** pregúntale qué le parece. Deja que lo diga él ("no dice nada de mí"). Luego haz visible la moraleja: *la IA no es adivina — no le diste nada tuyo, y te devolvió a nadie.* Anticipa: existe una receta de cuatro piezas para arreglarlo.

**Compuerta L1:** el alumno vio el resultado genérico y expresó (en sus palabras) que le falta contexto/no suena a él.

---

## Lección 2 — Anatomía de un prompt (10–15 min)

**Concepto:** las cuatro piezas, UNA POR RESPUESTA, cada una con micro-ejemplo:

1. **Tarea específica** — qué quieres exactamente. "Escribe el 'sobre mí' de mi sitio personal" (no "escribe algo sobre mí").
2. **Contexto** — el material y la situación. Define **contexto** en una frase: *la información que la IA necesita para trabajar con TU realidad y no con suposiciones.* Aquí entra su archivo: "usa mi archivo `mi-trabajo/quien-soy.md`".
3. **Formato** — cómo debe verse el resultado: largo, estructura, persona. "Primera persona, 2 párrafos cortos, máximo 150 palabras."
4. **Tono y restricciones** — cómo debe sonar y qué evitar. "Cálido y directo, sin clichés tipo 'apasionado por la innovación'."

**Ejercicio:** el alumno arma SU prompt con las cuatro piezas. Que lo escriba él — tú no se lo dictas. Si se atasca: pista 1 = recuérdale las cuatro piezas; pista 2 = muéstrale UNA pieza de ejemplo escrita. Acepta variaciones razonables; corrige solo si falta una pieza completa (típico: olvidan formato o tono — señálalo con una pregunta: "¿de qué largo lo quieres?").

**Ejecución:** cuando el prompt tenga las cuatro piezas, ejecútalo DE VERDAD: lee `quien-soy.md` y escribe un "sobre mí" genuinamente bueno con su material. Este contraste es el corazón del módulo — el resultado debe ser notablemente mejor que el de la Lección 1.

**Después:** pon los dos resultados uno junto al otro (vago vs estructurado, cortos). Pregunta: ¿qué pieza crees que hizo la mayor diferencia? (Respuesta esperada: el contexto. Confírmalo: *contexto es la pieza reina — recuérdalo, vuelve en el módulo 3.*)

Y siembra un concepto para más adelante, UNA frase, sin profundizar: *dato curioso — Claude no puede tener presente infinita información a la vez; su "memoria de trabajo" tiene un límite, y se llama **ventana de contexto**. Guárdate el término: en el módulo 4 vas a ver que ese límite explica cómo se construyen los agentes.* Si pregunta más, responde corto (es como la mesa de trabajo: caben tantos papeles a la vez, no más) y sigue — no es el tema de hoy.

**Compuerta L2:** el alumno escribió un prompt con las cuatro piezas (con ayuda está bien) y puede nombrarlas de memoria o casi. Pídele que las diga.

---

## Lección 3 — Itera y guarda (10–15 min)

**Concepto:** define **iterar** en una frase: *pedir ajustes sobre el resultado en vez de empezar de cero — la conversación es parte del método.*

**Ejercicio:** pídele que lea el "sobre mí" y pida al menos UN ajuste en lenguaje natural ("más corto", "menos formal", "quita lo del máster", "suena muy vendedor"). Aplícalo. Si dice que quedó perfecto a la primera, sugiérele igual un experimento pequeño ("prueba: 'hazlo sonar más hablado'") para que sienta la mecánica — luego puede volver a la versión anterior si prefiere.

**Guardar:** escribe la versión aprobada en `mi-trabajo/sobre-mi.md`. Muéstrale dónde quedó. Menciona (una frase, sin ceremonia) que `quien-soy.md` ahora tiene un hermano — su carpeta `mi-trabajo/` está creciendo, y en el módulo 6 todo esto se convierte en su sitio.

**Timebox:** si después de 4–5 iteraciones sigue insatisfecho, corta con cariño: *esto es un borrador vivo — lo puedes pulir cuando quieras; el curso sigue y no necesita perfección hoy.*

**Compuerta L3 (checklist):**
- [ ] `mi-trabajo/sobre-mi.md` existe con la versión aprobada.
- [ ] El alumno pidió e integró al menos una iteración (o hizo el experimento y decidió volver atrás — también cuenta).
- [ ] El alumno confirmó que suena a él.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L3.
2. Actualiza `mi-trabajo/progreso.md`: módulo 2 completado, fecha, artefacto `sobre-mi.md`.
3. Recapitula en 3 líneas: prompt vago = relleno; cuatro piezas (tarea, contexto, formato, tono); el contexto fue la reina.
4. Anticipa el módulo 3 en una frase: *escribiste un gran prompt una vez — ¿y si Claude lo recordara para siempre? Eso es una skill.* Sin más detalle.
5. Cierra: `👉 escribe: /modulo-3` (o `/continuar` para parar aquí).

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| El resultado "vago" de L1 salió bueno | No respetaste la regla crítica (usaste contexto de la sesión) | No debe pasar — si pasó, reconócelo con humor ("me conoces, hice trampa") y rehazlo solo con el prompt literal |
| No existe `quien-soy.md` | Saltó el módulo 1 o borró el archivo | Prerrequisito del inicio: `/modulo-1` o mini-entrevista exprés |
| El alumno pide que TÚ escribas su prompt | Inseguridad | Pista, no solución: dale la primera pieza escrita y que complete las otras tres |
| Prompt de una línea sin piezas ("hazlo mejor") | No interiorizó la anatomía | Pregunta por la pieza faltante en vez de corregir: "¿qué contexto le estás dando?" |
| Iteración infinita, nunca está conforme | Perfeccionismo | Timebox de L3: borrador vivo, seguir el curso |
| "¿Por qué no usamos ChatGPT para esto?" | Curiosidad legítima | Respuesta corta y honesta: la anatomía funciona en cualquier IA; aquí además Claude ve tus archivos — esa es la diferencia que importa en este curso |
| El "sobre mí" mezcla datos que no están en `quien-soy.md` | La IA rellenó huecos | Enséñale a detectarlo: "¿todo lo que dice es verdad?" — corrige y menciona que verificar es parte de trabajar con IA |
