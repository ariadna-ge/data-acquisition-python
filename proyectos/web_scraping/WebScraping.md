# Web Scraping de Leyes Vigentes en México

## Objetivo
Realizar un proceso de adquisición de datos mediante Web Scraping sobre el portal de leyes vigentes de la Cámara de Diputados, extrayendo información estructurada de las leyes federales mexicanas y descargando automáticamente los documentos PDF del texto vigente.

* **Fuente de datos:** [Leyes Federales Vigentes - Cámara de Diputados](http://www.diputados.gob.mx/LeyesBiblio/index.htm)

## Desarrollo de la Práctica
Este resuelven los 7 puntos solicitados:

1. **Consumo de la página HTML:** Se realiza la petición HTTP a la URL base incluyendo un encabezado (`User-Agent`) y se valida que la respuesta sea correcta.
2. **Análisis de la estructura del sitio:** Se procesa el HTML descargado para ubicar las tablas y filas que contienen la información.
3. **Extracción de la información:** Se extraen los datos de las leyes vigentes iterando sobre el HTML para construir una lista de diccionarios con los campos requeridos:
   * `numero`: Número consecutivo
   * `nombre_ley`: Nombre de la ley
   * `fecha_publicacion`: Fecha DOF
   * `ultima_reforma`: Fecha de última reforma
   * `url_pdf`: URL del PDF vigente
   * `url_doc`: URL DOC (si existe)
   * `url_epub`: URL EPUB (si existe)
4. **Creación del DataFrame:** La lista de diccionarios con la información de las leyes se convierte en un DataFrame de Pandas para su manipulación.
5. **Descarga de PDFs:** Descargar automáticamente los PDF del texto vigente en el directorio `/content/drive/MyDrive/add/leyes/pdf_{fechahora}/`, nombrando cada archivo mediante el número y el nombre simplificado de la ley (por ejemplo: `001_constitucion.pdf`).
6. **Almacenamiento de información:** Los datos tabulares procesados se guardan directamente en Google Drive en la ruta `/content/drive/MyDrive/add/leyes/datos`.
7. **Logging:** Se genera un logging en formato JSON a lo largo de la ejecución para llevar el registro del proceso.

## Información Académica
* **Institución:** FES Aragón UNAM
* **Carrera:** Ingeniería en Computación
* **Asignatura:** Adquisición de Datos
* **Alumna:** Ariadna Denisse García Estrada