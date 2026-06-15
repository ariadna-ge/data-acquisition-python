# Procesamiento de Datos: Apache Spark (RDDs)
*Introducción a la computación distribuida usando el núcleo de Apache Spark (RDDs).*
Notebook enfocado en el paradigma de programación de Spark utilizando RDDs (Resilient Distributed Datasets). Incluye transformaciones, acciones y conteo de palabras distribuido.
`ADD_20262_08_Spark.ipynb`

## Características:
- Creación y manipulación de RDDs (Resilient Distributed Datasets).
- Diferenciación clara entre transformaciones (perezosas) y acciones (inmediatas).
- Cálculo distribuido mediante operaciones map, reduce y filter.
- Monitoreo de ejecución en el Spark UI.

# Procesamiento de Datos: Spark DataFrames
*Procesamiento de Big Data utilizando la API de DataFrames de Apache Spark.*
Implementación de lógica de procesamiento de grandes volúmenes de datos utilizando Spark SQL y DataFrames. Incluye ejemplos de consultas estructuradas sobre archivos Parquet.
`ADD_20262_Spark_DataFrame.ipynb`

## Características:
- Carga eficiente de archivos Parquet masivos.
- Aplicación de transformaciones (filter, select, groupby) optimizadas para clústeres.
- Consultas SQL directamente sobre DataFrames mediante spark.sql.
- Limpieza y manejo de valores nulos a gran escala.