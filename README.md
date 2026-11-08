# Q-Music nativa (gratis, sin App Store)

Es una app nativa de iPhone (Swift + WKWebView) que muestra tu app web a pantalla completa real,
con audio en segundo plano. Se firma con tu Apple ID gratuito y **AltStore la renueva sola**.

Tu MacBook Air 2017 no puede usar Xcode 15 (el que soporta iPhone con iOS 17/18), así que
**la compilación la hace GitHub gratis en la nube**. Solo necesitas el Mac para instalar y renovar.

## Paso 1 · Tener tu app web alojada (HTTPS)
Sube la carpeta `Marginalia-main` a GitHub Pages (o Netlify). Anota la URL final, con la barra
del final, por ejemplo `https://tuusuario.github.io/Marginalia/`.
Registra esa misma URL en el panel de Spotify Developer → Redirect URIs.

## Paso 2 · Compilar el .ipa en GitHub (sin Xcode)
1. Crea un repositorio **público** (así los minutos de macOS son gratis) y sube el contenido de esta carpeta.
2. Entra a la pestaña **Actions** → «Compilar IPA» → **Run workflow**.
3. Escribe la URL del paso 1 y ejecútalo. Tarda unos 5–8 minutos.
4. Descarga el artefacto `QMusic-ipa` (es un zip con `QMusic.ipa`).

## Paso 3 · Instalar en el iPhone con AltStore
1. En el Mac instala **AltServer** desde altstore.io y sigue su guía (en macOS Monterey instala el plug-in de Mail).
2. En el iPhone: Ajustes → Privacidad y seguridad → **Modo desarrollador** (activar y reiniciar).
3. Conecta el iPhone por cable, desde el icono de AltServer elige «Install AltStore» con tu Apple ID.
4. Abre AltStore en el iPhone → «My Apps» → «+» → elige `QMusic.ipa`.

## Renovación automática
AltStore renueva las apps en segundo plano cada pocos días **si el Mac está encendido, con AltServer
abierto y en la misma Wi‑Fi que el iPhone**. Si pasas más de 7 días sin eso, la app deja de abrir
y basta reinstalarla desde AltStore (tus datos de la web no se pierden).

## Límites del Apple ID gratuito
Máximo 3 apps instaladas a la vez y 10 identificadores nuevos por semana.

## Nota
El código no se pudo compilar en el entorno donde se escribió (no hay Xcode). Si la compilación en
GitHub falla, copia el error del paso que falle y se corrige.
