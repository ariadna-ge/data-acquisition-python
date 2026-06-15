# Pipeline de Adquisición: NoSQL (MongoDB)

Este notebook gestiona la extracción de documentos desde una colección de MongoDB, realiza normalización de esquemas irregulares (JSON anidado) y exporta los datos procesados a formato AVRO.

## Características
* Conexión a MongoDB con `pymongo`.
* Normalización de datos: Uso de `df.explode()` y aplanamiento de estructuras anidadas.
* Mapeo de catálogos: Estandarización de materias y calificaciones.
* Exportación: Serialización a formato AVRO utilizando `fastavro`.
* Carga Analítica: Inserción de métricas calculadas en una tabla SQL de destino.