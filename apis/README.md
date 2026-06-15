# Adquisición de Datos: Consumo de APIs (GraphQL/REST)
*Automatización de la recolección de datos mediante el consumo de servicios web.*

Este notebook demuestra la ingesta de datos consultando APIs externas (ej. GraphQL). Se enfoca en la estructuración de peticiones y transformación de respuestas JSON a DataFrames.

## Características:
- Manejo de autenticación para APIs protegidas.
- Implementación de peticiones GET/POST.
- Transformación de respuestas anidadas de formato JSON a DataFrames planos.
- Control de errores HTTP (404, 500, etc.) mediante raise_for_status().