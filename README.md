Modelo predictivo en Apache Spark MLlib

Modelo de clasificación binaria construido con PySpark y MLlib para predecir si una transacción de venta es riesgosa (1) o normal (0), a partir de un dataset de ventas simuladas.

## ¿Qué hace este proyecto?

- **Limpieza de datos:** el dataset original traía valores corruptos (fechas en columnas numéricas, campos vacíos), por lo que se aplicó un proceso de casteo, reconstrucción y filtrado de datos.
- **Preparación:** se creó una columna `label` con una regla de negocio simple (monto alto o venta en madrugada) y se construyeron las `features` con `StringIndexer` + `VectorAssembler` dentro de un `Pipeline`.
- **Entrenamiento:** se entrenó un modelo de **Regresión Logística**, con división de datos en entrenamiento (80%) y prueba (20%).
- **Evaluación:** se calcularon métricas de Accuracy, F1-score y areaUnderROC, junto con un análisis crítico de los resultados (se detectó y documentó un caso de *data leakage*).

## Tecnologías utilizadas

- Apache Spark / PySpark
- Spark MLlib (StringIndexer, VectorAssembler, Pipeline, LogisticRegression)
- Google Colab

## Archivos

- `Prueba_Modelo_Predictivo_Spark_MLlib.ipynb`: notebook completo con el desarrollo, código comentado y resultados.
- `ventas_simuladas.csv`: dataset utilizado.
