# Clasificación automática de noticias mediante Machine Learning y NLP

## 1. Descripción del proyecto

Este proyecto desarrolla un sistema de clasificación automática de noticias mediante técnicas de Machine Learning y Procesamiento de Lenguaje Natural (NLP).

El objetivo es clasificar noticias según su contenido textual en cuatro categorías: **Business, Sci_Tech, Sports y World**.

El trabajo integra las principales etapas de un proyecto de Machine Learning: formulación del problema, análisis exploratorio de datos, preprocesamiento textual, entrenamiento y comparación de modelos, optimización de hiperparámetros, evaluación, análisis de errores y explicabilidad mediante SHAP.

## 2. Objetivo y formulación del problema

Se aborda un problema de **clasificación multiclase supervisada**.

- **Variable de entrada:** `text`, que contiene el texto de cada noticia.
- **Variable objetivo:** `label`, que identifica la categoría de la noticia.
- **Métrica principal:** F1-score macro.
- **Métricas complementarias:** accuracy, precision y recall.

Se utiliza F1-score macro porque calcula el F1-score de cada categoría y les asigna el mismo peso, lo que permite evaluar el desempeño del modelo sin favorecer a las clases más frecuentes.

La clasificación automática de noticias puede facilitar la organización de grandes volúmenes de información y mejorar la búsqueda y recuperación de contenidos.

## 3. Datos utilizados

El proyecto utiliza un conjunto de noticias dividido en entrenamiento y prueba:

- **Entrenamiento:** 8.000 registros.
- **Prueba:** 2.000 registros.
- **Cantidad de categorías:** 4.

Las categorías son:

- `Business`: negocios y economía.
- `Sci_Tech`: ciencia y tecnología.
- `Sports`: deportes.
- `World`: noticias internacionales.

El conjunto de entrenamiento se divide, a su vez, en entrenamiento y validación.
