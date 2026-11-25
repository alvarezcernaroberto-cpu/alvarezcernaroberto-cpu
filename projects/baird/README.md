# Baird

Asistente personal con IA ejecutado en local.

## Qué hace

- Responde por Telegram y Alexa.
- Guarda memoria persistente (SQLite).
- Decide por niveles qué modelo usar según la complejidad: Gemini → Claude → OpenRouter / Groq, para optimizar costo y latencia.
- Incluye enrutador gratuito para fecha, hora, clima y recordatorios.

## Stack

Python · Gemini · Claude · OpenRouter / Groq · SQLite · Telegram Bot API

## Estado

En desarrollo activo. Actualmente estoy reescribiendo su arquitectura alrededor de un orquestador que decide qué herramienta ejecutar en cada petición.

## Nota

El código completo vive en su propio proyecto local. Esta carpeta es la presentación del proyecto dentro de `gamer-dev`, no un duplicado del código.
