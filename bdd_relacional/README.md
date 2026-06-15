# Pipeline de Adquisición: Base de Datos Relacional (MySQL)

Este notebook implementa un proceso ETL (Extracción, Transformación, Carga) para extraer datos de alumnos desde una base de datos MySQL relacional y almacenarlos en formato Parquet.

## Características
* Conexión a MySQL mediante `sqlalchemy`.
* Extracción incremental basada en el año de edición.
* Transformación de datos: Concatenación de nombres y limpieza de columnas.
* Auditoría: Registro de eventos en un archivo de log (`logs_adquisicion.log`).
* Almacenamiento en Data Lake (Google Drive) en formato Parquet.