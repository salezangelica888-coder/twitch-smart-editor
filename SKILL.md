---
name: twitch-smart-vod-editor
description: Descarga VODs de Twitch y los edita usando transcripción inteligente para conservar chistes y jugadas del juego, eliminando silencios muertos y donaciones.
---

# Instrucciones de Edición Inteligente para VODs de Twitch

Cuando el usuario te pida editar un VOD de Twitch, sigue estrictamente este flujo de trabajo paso a paso:

## 1. Descarga del VOD
- Usa `yt-dlp` para descargar el video o el tramo de tiempo indicado por el usuario en formato MP4.

## 2. Transcripción y Análisis de Contexto (Whisper)
- Extrae el audio y usa `Whisper` para generar una transcripción completa con marcas de tiempo exactas (segundo a segundo).
- Lee toda la transcripción como un editor profesional de YouTube para gaming.
- **CONSERVAR:** Chistes, historias divertidas, reacciones genuinas, gritos de emoción y momentos con hilo narrativo.
- **ELIMINAR:** Pausas aburridas, tiempos muertos sin hablar, saludos repetitivos al chat y cualquier agradecimiento de donaciones, bits o suscripciones.

## 3. Protección de Jugadas del Juego (Regla Crítica)
- Antes de eliminar cualquier fragmento donde el streamer esté en silencio, analiza la pista de audio y el movimiento visual del video.
- **NUNCA borres** un segmento si hay sonidos intensos del juego (disparos, explosiones, efectos de habilidades, música de combate) o cambios rápidos de escena en pantalla, aunque no haya voz.
- Deja siempre un margen de seguridad de **1.5 segundos** antes y después de cada jugada o chiste para evitar cortes bruscos.

## 4. Renderizado Final
- Usa `FFmpeg` para recortar y unir únicamente los clips aprobados.
- Entrega el archivo final en MP4 listo para descargar.
