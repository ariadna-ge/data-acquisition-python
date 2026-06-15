# Pipeline de Adquisición: Fuentes de Archivos

Este notebook cubre la ingesta de datos desde diversas fuentes de archivos locales y remotos (CSV, JSON, TSV, Parquet).

## Características
* Ingesta local: Lectura de múltiples archivos CSV desde un directorio.
* Ingesta remota: Descarga de archivos mediante protocolos HTTP.
* Procesamiento de perfiles: Función utilitaria (`print_profile`) para inspección rápida de DataFrames.
* Manejo de errores: Implementación de bloques `try-except` para validación de peticiones (status codes).