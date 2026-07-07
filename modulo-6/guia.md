# Guía interna — Módulo 6: Publicar: tu sitio en vivo

> **Reglas (recordatorio):** un concepto a la vez · compuerta antes de avanzar · pista → parcial → completa (solo si la piden tras dos pistas) · nunca leer esta guía al alumno · cada respuesta termina con 👉 · al cerrar compuerta, actualizar `mi-trabajo/progreso.md`.

## Objetivo

Al terminar, el alumno tiene su sitio personal publicado en una URL real de internet, y el curso completo queda cerrado con calidez.

**Prerrequisito:** `mi-trabajo/paquete-de-contenido-final.md` (módulo 5). Verifícalo antes de empezar; si falta, dirige a `/modulo-5`.

**Regla técnica crítica para ti (el tutor), no para el alumno:** la sesión de Claude Code **se queda en la carpeta del curso durante todo el módulo**. El sitio se construye dentro de `mi-trabajo/mi-sitio/` usando rutas — NUNCA le pidas al alumno que cierre esta sesión y abra Claude Code en otra carpeta. Si sale de aquí, pierde el CLAUDE.md, los comandos, y el progreso justo en el cierre del curso.

---

## Lección 1 — De contenido a sitio (10–15 min)

**Concepto:** define **sitio estático** en una frase — *una página web que es solo un archivo (HTML): el navegador la lee directo, sin necesitar un servidor especial detrás.* Y una frase sobre la herramienta de estilo: *vamos a usar Tailwind, una caja de herramientas de diseño que se activa con una sola línea — no hay que instalar nada.*

**Acción (tú la haces, con el alumno mirando):**

1. Crea la carpeta `mi-trabajo/mi-sitio/`.
2. Copia `modulo-6/starter/index-plantilla.html` a `mi-trabajo/mi-sitio/index.html`.
3. Lee `mi-trabajo/paquete-de-contenido-final.md` y rellena la plantilla con el contenido real del alumno: nombre y tagline en el header, y las cinco secciones (Sobre mí, Proyectos, Experiencia, Habilidades, Contacto). Sin estilo todavía — solo contenido real en su lugar.

**Muéstrale cómo verlo:** dile que abra `mi-trabajo/mi-sitio/index.html` haciendo doble clic (o arrastrándolo a una pestaña del navegador). Va a verse simple, sin colores ni diseño — normal, eso es justo lo que sigue.

**Compuerta L1:** `mi-trabajo/mi-sitio/index.html` existe, con el contenido real del alumno en las cinco secciones (no placeholders), y el alumno confirmó que lo abrió y lo vio en su navegador.

---

## Lección 2 — Vibe coding: hazlo tuyo (15–25 min)

**Concepto:** define **vibe coding** en una frase — *en vez de escribir estilos línea por línea, le describes a Claude cómo quieres que se vea o se sienta tu sitio, ves el resultado, y ajustas hablando — igual que iteraste tu "sobre mí" en el módulo 2, pero ahora con diseño.*

**Preguntas para arrancar (una a la vez, sin ametrallar):**

- ¿Qué colores te representan? (si no sabe, ofrece 2–3 direcciones simples: "minimalista con un solo color de acento", "cálido con tipografía grande", "oscuro y elegante")
- ¿Hay algún sitio que te guste visualmente, tuyo o de alguien más? (opcional — si no tiene, sigue sin problema con lo anterior)
- ¿Serio/profesional o más personal/informal?

**Aplica los cambios con clases de Tailwind** directamente en el HTML: colores de fondo y texto, tipografía, espaciado, formas de botones y tarjetas. Cambia, guarda, y dile que recargue el navegador (F5) para ver el resultado.

**El ciclo es el mensaje:** pide un cambio → aplica → recarga y mira → ajusta. Repite 2–4 veces. Si a la primera dice que le encanta, está perfecto — no lo obligues a iterar por iterar.

**Compuerta L2:** el alumno confirmó, con sus palabras, que el sitio ya se siente suyo (no el de nadie más) — tras al menos una ronda de ajuste.

---

## Lección 3 — Publícalo (10–15 min)

**Concepto:** define **desplegar/publicar** en una frase — *sacar el archivo de tu computadora y ponerlo en un servidor de internet, para que cualquiera con el link lo pueda ver.* Vamos a usar Vercel, con un solo comando — sin cuenta de GitHub.

**Pasos:**

1. Verifica que exista `npx` (viene con Node.js). Si no existe, ve a la tabla de atascos.
2. Desde la carpeta del curso, ejecuta el despliegue apuntando a `mi-trabajo/mi-sitio` (por ejemplo `npx vercel mi-trabajo/mi-sitio`). La primera vez pedirá iniciar sesión (por correo o cuenta existente — no hace falta GitHub) y confirmar la configuración del proyecto — acepta los valores por defecto.
3. Obtendrás una URL de vista previa. Para la URL definitiva, ejecuta el despliegue de producción (`npx vercel --prod` desde `mi-trabajo/mi-sitio`, o el flag equivalente vigente).

**Verificación real:** pídele al alumno que abra la URL en el navegador (idealmente desde el teléfono también, para que sienta que es de verdad "internet", no solo su computadora).

**Compuerta L3:** el alumno tiene una URL real, la abrió, y su sitio carga correctamente.

---

## Lección 4 — Compártelo (10 min) — cierre del curso completo

**Concepto:** en una frase — *la galería del curso es donde otros aprendices ven lo que construiste, y donde tú ves lo que construyeron ellos.*

**Invita, sin presionar:**

1. Compartir la URL en la galería del curso (Discussions del repositorio).
2. Publicar en redes con el hashtag **#CCenEspañol**, si quiere.

Si prefiere no compartir todavía, está bien — el curso se cierra igual con calidez; puede volver a compartir cuando quiera.

**Cierre del curso completo (Beat final):**

1. Recapitula los seis módulos en pocas líneas: fundamentos → prompts → skills → agentes y la ventana de contexto → orquestación (equipo en paralelo + corrector universal) → un sitio real, en internet, hecho por ti.
2. Nombra la lección transferible: *no aprendiste a usar UNA herramienta — aprendiste a pedir bien, a guardar lo que funciona, a delegar trabajo, y a coordinar varias piezas a la vez. Eso sirve para cualquier proyecto que hagas de aquí en adelante, no solo para este sitio.*
3. Felicita de verdad — publicó un sitio, en vivo, con su URL.
4. Cierre cálido, sin más "próximo paso" técnico — el curso terminó. Si quiere seguir, menciona la Ruta PM como opción disponible.

**Compuerta L4 (checklist final del curso):**
- [ ] El alumno tiene una URL en vivo funcionando.
- [ ] Se le invitó a compartir en la galería y con el hashtag (aceptó o declinó — ambas están bien).
- [ ] `mi-trabajo/progreso.md` marca el módulo 6 y el curso como completados.

---

## Compuerta de cierre del módulo

1. Verifica la checklist de L4.
2. Actualiza `mi-trabajo/progreso.md`: módulo 6 completado, fecha, URL del sitio, curso completo.
3. Sigue directo al cierre cálido descrito arriba — no hay módulo 7.

---

## Tabla de atascos

| Síntoma | Causa probable | Qué hacer |
|---------|----------------|-----------|
| Falta `paquete-de-contenido-final.md` | Saltó el módulo 5 | Dirige a `/modulo-5` |
| El sitio se ve sin estilo, solo texto plano, incluso tras la Lección 2 | Falta el `<script>` de Tailwind, o no hay conexión a internet (el CDN lo necesita) | Verifica que la etiqueta `<script src="https://cdn.tailwindcss.com">` esté en el `<head>`; confirma conexión a internet |
| `npx: command not found` o similar | No tiene Node.js instalado | Instalar Node.js desde nodejs.org (instalador simple, "LTS"), reiniciar la terminal, reintentar |
| El login de Vercel pide abrir un navegador y no puede | Sesión de terminal remota o sin navegador gráfico | Vercel permite iniciar sesión con un código en vez de navegador — sigue las instrucciones que muestra la terminal |
| Solo tiene una URL de "preview", no la definitiva | No corrió el despliegue de producción | Ejecuta el despliegue con la bandera de producción |
| Se siente abrumado eligiendo colores/estilo en la Lección 2 | Parálisis de decisión | Ofrece 2–3 direcciones simples predefinidas (ver Lección 2) en vez de un lienzo en blanco |
| Quiere agregar fotos reales | Fuera de alcance de hoy | Confirma que el sitio funciona sin fotos; agregarlas después es un ajuste simple, no bloquea publicar hoy |
| No quiere compartir en la galería | Timidez o prisa | Respeta la decisión — el curso se cierra igual; puede compartir cuando quiera |
