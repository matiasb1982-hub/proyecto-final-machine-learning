# Clasificación automática de noticias mediante Machine Learning y NLP

## Descripción del proyecto

Este proyecto desarrolla un sistema de clasificación automática de noticias mediante Machine Learning y Procesamiento de Lenguaje Natural (NLP).

El objetivo es clasificar noticias en cuatro categorías: Business, Sci_Tech, Sports y World, utilizando el texto como variable de entrada.

## Objetivo y métrica

Se trata de un problema de clasificación multiclase supervisada. La variable objetivo es `label` y el texto de entrada es `text`.

La métrica principal es el F1-score macro, complementada con accuracy, precision y recall.

## Datos

- Datos de entrenamiento: 8.000 noticias.
- Datos de prueba: 2.000 noticias.
- Categorías: Business, Sci_Tech, Sports y World.

El conjunto de prueba se reserva para la evaluación final del modelo.

## Metodología

El notebook incluye:

1. Formulación del problema.
2. Análisis exploratorio de datos (EDA).
3. Limpieza y preprocesamiento del texto.
4. Representación textual mediante TF-IDF.
5. División de datos para entrenamiento, validación y prueba.
6. Entrenamiento y comparación de modelos.
7. Optimización de hiperparámetros con GridSearchCV.
8. Evaluación final.
9. Análisis de errores.
10. Explicabilidad de predicciones mediante SHAP.
11. Evaluación complementaria de XGBoost con TF-IDF y SVD.
12. Conclusiones, limitaciones y reproducibilidad.

## Resultados

La comparación inicial en validación obtuvo los siguientes resultados de F1-score macro:

| Modelo | F1-score macro |
|---|---:|
| LinearSVC | 0,8926 |
| Regresión logística | 0,8869 |
| Multinomial Naive Bayes | 0,8855 |

La regresión logística optimizada obtuvo en el conjunto de prueba:

- Accuracy: 0,8905.
- Precision macro: 0,8907.
- Recall macro: 0,8905.
- F1-score macro: 0,8905.

Se registraron 219 predicciones incorrectas de un total de 2.000 noticias. Las confusiones más frecuentes se produjeron entre Business y Sci_Tech.

Los resultados corresponden a diferentes etapas de evaluación y deben interpretarse teniendo en cuenta sus respectivos conjuntos de datos.

## Requisitos

Las principales bibliotecas utilizadas son pandas, NumPy, matplotlib, seaborn, scikit-learn, XGBoost y SHAP. Sus versiones se encuentran documentadas en `requirements.txt` y en el notebook.

## Cómo ejecutar el proyecto

1. Obtener los datos utilizados por el notebook.
2. Abrir `Proyecto_Final_Machine_Learning.ipynb` en Google Colab o Jupyter.
3. Instalar las dependencias indicadas en `requirements.txt`.
4. Verificar las rutas de acceso a los datos.
5. Ejecutar las celdas en orden.

Para reproducir los resultados, se recomienda utilizar las mismas versiones de las bibliotecas y la semilla aleatoria documentada en el notebook.

## Estructura del repositorio

- `Proyecto_Final_Machine_Learning.ipynb`: código, análisis y resultados.
- `requirements.txt`: dependencias del proyecto.
- `README.md`: documentación e instrucciones de ejecución.

Los datos deberán incorporarse al repositorio si sus condiciones de uso lo permiten. En caso contrario, se deberán documentar las instrucciones para obtenerlos.

## Limitaciones

La clasificación puede presentar dificultades cuando una noticia aborda temas de varias categorías o utiliza vocabulario ambiguo. El desempeño también depende de la representatividad y actualidad de los datos.

## Conclusión

El proyecto integra las etapas principales de un flujo de Machine Learning para clasificación de texto, incluyendo evaluación cuantitativa, análisis de errores y explicabilidad mediante SHAP.

El notebook documenta el procedimiento y los resultados obtenidos para facilitar su revisión y reproducción.
