#   Predict Calorie Expenditure | Kaggle Competition Analysis

[![Kaggle](https://kaggle.com/static/images/site-logo.svg)](https://www.kaggle.com/competitions/predict-calorie-expenditure)

Este repositorio contiene el análisis y los notebooks desarrollados para mi participación en la competencia "Predict Calorie Expenditure" en Kaggle. El objetivo de la competencia fue predecir el gasto de calorías durante un entrenamiento.

##   Objetivo de la Competencia

El desafío principal consistió en construir un modelo capaz de predecir la cantidad de calorías quemadas por los usuarios durante sus sesiones de entrenamiento. Esto implicó el análisis de datos de entrenamiento, el manejo de diversas variables relacionadas con el ejercicio y los usuarios, y la construcción de modelos predictivos precisos.

##   Notebooks Incluidos

Este repositorio incluye los siguientes notebooks, que exploran diferentes estrategias para el análisis de datos, la ingeniería de características y el modelado:

1.  **`eda_modelado_ml_pce.ipynb`**: https://colab.research.google.com/drive/1fRNNKYtLuJ8SsO03hZkrQOq4XO0ey9He?usp=sharing
    * **Análisis Exploratorio de Datos (EDA):** Se realiza un EDA exhaustivo para identificar las características más relevantes para la predicción del gasto de calorías y explorar las relaciones entre las variables, incluyendo el impacto de las variables binarias en la quema de calorías.
    * **Ingeniería de Características:** Se generan nuevas características a través de combinaciones de variables existentes, segmentación por grupos de edad, cálculo del índice de masa corporal (IMC) y otras transformaciones relevantes.
    * **Modelado con Machine Learning:** Se implementan y comparan tres modelos de ML: XGBoost (XGB), LightGBM (LGBM) y Random Forest (RF). Se utiliza la búsqueda de cuadrícula (`GridSearchCV`) para optimizar los hiperparámetros de los modelos.
    * **Análisis de Importancia de Variables:** Se determina la importancia de cada característica en las predicciones del mejor modelo de ML.
    * **Reducción de Dimensionalidad:** Se aplican técnicas de reducción de dimensionalidad para crear dos componentes principales, buscando capturar información relevante y mejorar las predicciones al complementar las variables más importantes.

2.  **`redes_neuronales_pytorch_pce.ipynb`**: https://colab.research.google.com/drive/17ZcDPcrJ6XYbxcuuJId-NPTywirKTLxe?usp=sharing
    * **Implementación con PyTorch:** Se desarrollan modelos de redes neuronales utilizando la librería PyTorch para predecir el gasto de calorías.
    * **Reutilización de Ingeniería de Características:** Se aprovechan las características generadas en el primer archivo para entrenar las redes neuronales.
    * **Entrenamiento y Evaluación:** Se entrenan las redes neuronales y se evalúan sus resultados.

##   Estrategia de Combinación de Modelos

Se explora la combinación de los modelos de ML y NN con el objetivo de mejorar la precisión de las predicciones:

* Se generan predicciones utilizando los tres modelos de ML.
* Estas predicciones de ML se incorporan como características adicionales al conjunto de datos de entrenamiento para las redes neuronales.
* Se entrena nuevamente las redes neuronales con estas características adicionales.
* Se realiza la división del conjunto de datos en entrenamiento y prueba (train-test split) para evaluar el rendimiento de los modelos.

##   Resultados

En la evaluación final con el conjunto de datos de prueba de la competencia, se observó que la combinación de modelos (ML + NN) no produjo mejoras significativas en comparación con el uso exclusivo de los modelos de redes neuronales.

##   Conclusiones

Este proyecto demuestra un enfoque integral para la predicción del gasto de calorías, desde el análisis exploratorio de datos y la ingeniería de características hasta la implementación y comparación de modelos de machine learning y redes neuronales. Aunque la combinación de modelos no resultó en una mejora sustancial en este caso, el proyecto proporciona valiosas lecciones sobre el proceso de modelado y la importancia de la experimentación.
