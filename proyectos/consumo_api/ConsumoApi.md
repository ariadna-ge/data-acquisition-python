# Adquisición de Datos: Consumo de API REST de Banco de México

## Objetivo
Consumir la API REST del Sistema de Información Económica de Banco de México para consultar series económicas, obtener sus datos históricos dentro del rango disponible y almacenar los resultados en Google Drive.

**URL de la API:** [https://www.banxico.org.mx/SieAPIRest/service/v1/](https://www.banxico.org.mx/SieAPIRest/service/v1/)

## Requisitos del Proyecto

### 1. Token de Consulta
El token de consulta es un requisito necesario (64 caracteres alfanuméricos) que debe ser enviado a través del header HTTP `Bmx-Token`. Este token debe guardarse como variable de entorno o en un archivo `.env`.

### 2. Estructura de Datos (DataFrames)
Para cada serie descargada, se deberá crear un DataFrame de Pandas con al menos las siguientes columnas:
* `id_serie`: Identificador de la serie.
* `titulo`: Nombre de la serie.
* `fecha`: Fecha del dato.
* `valor`: Valor de la observación.

### 3. Almacenamiento en Google Drive
Los archivos se deben guardar en un directorio en Google Drive.
* **Directorio sugerido:** `/content/drive/MyDrive/add/banxico/`
* **Formatos a guardar por cada serie:**
  * `serie_<idSerie>.csv`
  * `serie_<idSerie>.json`
  * `serie_<idSerie>.parquet`

### 4. Logging
Generar un archivo de log con la información de la ejecución, preferentemente en formato JSON, con los siguientes campos mínimos:
* `run_id`: Identificador único de ejecución.
* `fecha_proceso`: Fecha y hora del proceso.
* `fuente`: Banco de México SIE API.
* `series_consultadas`: Lista de series descargadas.
* `registros_extraidos`: Total de registros descargados.
* `duracion`: Tiempo total de ejecución.
* `estado`: `success`, `warning` o `error`.

## Información Académica
* **Institución:** FES Aragón UNAM
* **Carrera:** Ingeniería en Computación
* **Asignatura:** Adquisición de Datos
* **Alumna:** Ariadna Denisse García Estrada