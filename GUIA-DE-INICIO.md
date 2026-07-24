# Guía de inicio (de cero a `/modulo-1`)

Esta guía te lleva de **nada instalado** a **escribir `/modulo-1` y empezar el curso**. No necesitas experiencia previa con la terminal ni con programación. Tiempo de lectura: ~5 minutos. Tiempo total: ~20-30 minutos, la mayoría esperando instaladores.

> **Antes de empezar:** necesitas una **suscripción de Claude** (plan Pro o superior, es de pago). El curso es gratis, pero la herramienta donde se enseña, Claude Code, requiere suscripción.

---

## Paso 1: Abre tu terminal

La terminal es una ventana de texto donde escribes comandos en vez de hacer clic. Se siente raro la primera vez. Es normal, solo vas a escribir (o pegar) algunas líneas.

### En Mac

Presiona `Cmd + Espacio` para abrir Spotlight, escribe `Terminal` y presiona Enter.

Deberías ver una ventana con un cursor parpadeando y texto parecido a `turnombre@MacBook ~ %`. Eso es todo, ya estás dentro.

### En Windows

Haz clic en el menú Inicio, escribe `PowerShell` y haz clic en **Windows PowerShell** (el ícono azul, no el de administrador; el normal está bien).

Deberías ver una ventana azul oscuro con un cursor parpadeando y texto como `PS C:\Users\tunombre>`. Eso es todo, ya estás dentro.

> **¿No funcionó?** En Mac, asegúrate de escribir "Terminal" exactamente. En Windows, si PowerShell no aparece, busca "Windows PowerShell" con el nombre completo.

---

## Paso 2: Instala Claude Code

Claude Code es la versión de terminal de Claude, la que usamos en todo el curso.

### En Mac o Linux

Pega esto en la Terminal y presiona Enter:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

### En Windows

Pega esto en PowerShell y presiona Enter:

```powershell
irm https://claude.ai/install.ps1 | iex
```

> **Si PowerShell bloquea el comando** con un error sobre "execution policy" o "no se puede cargar porque la ejecución de scripts está deshabilitada": cierra PowerShell, ábrelo de nuevo como administrador (clic derecho → "Ejecutar como administrador"), y ejecuta primero `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`, confirma con `S`, y luego repite el comando de instalación en una ventana normal (no admin).

Cualquiera de los dos comandos descarga e instala Claude Code. Toma uno o dos minutos.

Cuando termine, **cierra tu terminal y ábrela de nuevo** (así detecta el comando nuevo). Luego confirma:

```bash
claude --version
```

Deberías ver un número de versión.

> **¿No funcionó?** Reabrir la terminal es el arreglo más común. Si `claude --version` sigue sin funcionar, revisa la guía oficial en [claude.com/claude-code](https://claude.com/claude-code) para tu sistema operativo.

---

## Paso 3: Descarga el curso

No necesitas saber usar git: puedes descargar el curso como un archivo comprimido.

### Opción A: sin git (más simple)

En la página del repositorio en GitHub, haz clic en el botón verde **"Code"** → **"Download ZIP"**. Descomprime el archivo donde quieras (por ejemplo, tu carpeta de Escritorio) y recuerda el nombre de la carpeta resultante.

### Opción B: con git (si ya lo tienes)

```bash
git clone https://github.com/hfritz/claude-code-en-espanol.git
```

Esto descarga el curso a una carpeta nueva en tu ubicación actual.

---

## Paso 4: Entra a la carpeta del curso desde la terminal

Ahora necesitas que tu terminal "esté parada" dentro de la carpeta que acabas de descargar, porque ahí viven los archivos especiales (`.claude/`) que hacen que el curso funcione.

La forma más simple en cualquier sistema: escribe `cd ` (con un espacio al final, sin presionar Enter todavía), **arrastra la carpeta del curso desde el Finder (Mac) o el Explorador de archivos (Windows) y suéltala sobre la ventana de la terminal.** Esto escribe la ruta completa automáticamente. Presiona Enter.

Tu terminal debería mostrar que ahora estás dentro de esa carpeta (el nombre de la carpeta aparece en el prompt).

> **¿No funcionó?** Puedes confirmar dónde estás con `pwd` (Mac) o `pwd` / `Get-Location` (Windows). Si el nombre de la carpeta no coincide con la del curso, repite el arrastre.

> **Nota sobre carpetas ocultas:** dentro de la carpeta del curso hay una carpeta `.claude/` (el punto al inicio la hace invisible en el Finder y el Explorador por defecto). No necesitas verla ni tocarla, Claude la lee directamente. Ignórala.

---

## Paso 5: Escribe `claude`

Con la terminal parada dentro de la carpeta del curso, escribe:

```bash
claude
```

y presiona Enter.

La primera vez te pedirá **confiar en la carpeta** (di que sí) e **iniciar sesión**: tu navegador se abrirá automáticamente. Inicia sesión con la cuenta que tiene tu suscripción, haz clic en **Autorizar**, y vuelve a la terminal.

> **¿No funcionó?** Si el navegador no se abrió, copia la URL que imprimió la terminal y pégala manualmente en tu navegador. Si el login falla, confirma que usaste el correo de tu suscripción Pro.

---

## Paso 6: Escribe `/modulo-1`

Con Claude Code abierto y esperando tu mensaje, escribe:

```
/modulo-1
```

y presiona Enter. Claude te da la bienvenida y te guía al primer módulo. A partir de aquí, el curso se encarga de todo.

> **¿No funcionó?** Si Claude responde como un asistente genérico y no reconoce el curso, probablemente abriste `claude` desde la carpeta equivocada. Escribe `/exit`, repite el Paso 4, y vuelve a escribir `claude`.

---

## Ya estás dentro

Eso es toda la instalación. Todo lo demás pasa dentro de Claude Code. A construir.
