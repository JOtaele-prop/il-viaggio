# Reglas de diseño · Il Viaggio Arcade

- **Nada de emojis de librerías públicas** (Apple, Google, Twemoji, etc.). Todo icono nuevo es pixel art estilo arcade propio, dibujado en el código: añádelo a `PXICONS` (rejilla de 12×12 con la paleta `PXPAL`). Los emojis que tengan icono en `PXICONS` se cambian solos por la versión pixel en las ventanas.
- **La professoressa tiene que reconocerse a simple vista**: retrato pixel con nombre en la lección y, en el mapa, gafas, libro en la mano, pelo largo (si es profesora) y birrete flotando.
- Paleta de 16 colores del juego; las fuentes son Press Start 2P (títulos) y VT323 (texto).
- **Voz**: usar siempre `speak()`/`speakDone()` (cola por frases en `speakQ`); no crear `SpeechSynthesisUtterance` a mano, porque en Android se corta.
- **Traducir palabras**: tocar texto en cualquier ventana (o mantener pulsado, también sobre botones) abre `#wpop`. Se traduce primero con el diccionario del propio juego y, si no, en línea con caché.
- **Legible en el móvil y sin scroll infinito**: las tablas se hacen con `chTable` o `kvTable` (cabecera, etiqueta con nota, columnas fijas; nunca se salen de la pantalla). Las pantallas largas van en pestañas (como el Dossier) o en desplegables `<details class="pg">`, con lo actual abierto y lo demás plegado.
