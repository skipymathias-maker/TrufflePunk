# TRUFFLEMIX // DEMA

Reproductor de audio **100% local** (sin YouTube ni streaming) con estética cyberpunk + trinchera.
Añade archivos de audio, se guardan en el dispositivo; playlists, favoritos, búsqueda, aleatorio,
repetir, visualizador y controles en pantalla de bloqueo.

## Obtener el APK

### Opción A — GitHub Actions (sin instalar nada)
1. Crea un repositorio en GitHub y sube el contenido de esta carpeta.
2. Pestaña **Actions → Build APK** (corre sola al hacer push, o "Run workflow").
3. Descarga el artefacto **TruffleMix-debug-apk** → `app-debug.apk` → instálalo en tu Android
   (permite "instalar apps de origen desconocido").

### Opción B — Android Studio
Abre esta carpeta como proyecto → **Build ▸ Build APK(s)**. Sale en `app/build/outputs/apk/debug/`.

### Opción C — Línea de comandos
Con JDK 17 y Android SDK (API 34): `gradle assembleDebug`.

## Sin compilar
`app/src/main/assets/index.html` funciona tal cual en cualquier navegador moderno (también se puede
"Añadir a pantalla de inicio" en Chrome).

## Notas
- Formatos: lo que soporte el WebView de Android (mp3, m4a/aac, ogg, opus, wav, flac).
- Lee título, artista y carátula de las etiquetas ID3 de los MP3.
- Si no hay carátula, genera una portada procedural estilo trinchera.
