# 7506R-2C2022-GRUPO22

Materia Organizacion de Datos de la Facultad de Ingenieria de Buenos Aires.

Los trabajos prácticos se realizaron utilizando un conjunto de datos reales proporcionados por la plataforma Properati, que contiene información sobre propiedades en venta en la República Argentina durante el año 2021. Estos datos, extraídos de BigQuery, incluyen una variedad de características relacionadas con los anuncios inmobiliarios, como el precio, la ubicación y las descripciones de las propiedades.

El objetivo principal fue aplicar técnicas avanzadas de ciencia de datos, como el análisis exploratorio, preprocesamiento, clasificación y regresión, sobre este dataset real de la industria inmobiliaria. A lo largo de los trabajos, se buscó construir modelos predictivos y generar insights valiosos a partir de los datos proporcionados, abordando problemas tanto de clasificación como de regresión en diferentes escenarios.

Este trabajo fue desarrollado en una notebook de Python y todos los resultados son reproducibles. El código, modelos entrenados y datasets utilizados están disponibles en este repositorio.

## Integrantes:
    Joaquin Rivero - 106032
    Francisco Sobral - 108603
    Federico Forte - 92389
    Ian Klaus von der Heyde - 107638
    Juan Pablo Aschieri - 108000

Nota: Los modelos de clasificacion ocupan mucho espacio, por lo que les dejamos un link a un Drive para que los tengan https://drive.google.com/drive/folders/1fULXIU73I-AO75Jw6fXwhcsdVTLY4EsX?usp=sharing

## Trabajo Práctico 1: Precios de Propiedades

### Introducción

En este trabajo práctico se abordó un problema real de ciencia de datos utilizando un conjunto de datos de propiedades en venta en Argentina, provisto por Properati. Se realizaron las siguientes etapas:

### Parte 1, Análisis Exploratorio y Preprocesamiento de Datos:

- Se seleccionaron y limpiaron los datos, filtrando solo las propiedades de tipo vivienda en Capital Federal cuyo precio esté en dólares. Se manejaron valores faltantes, se detectaron y trataron valores atípicos, y se aplicó reducción de dimensionalidad.

### Parte 2, Agrupamiento:

- Se aplicó el algoritmo K-Means para analizar patrones y agrupar las propiedades en función de distintas características. Además, se evaluó la calidad de los grupos utilizando el análisis de Silhouette.

### Parte 3, Clasificación:
- Se clasificaron las propiedades en tres categorías de precio (alto, medio, bajo) según el precio por metro cuadrado. Para ello, se entrenaron modelos como Árbol de Decisión y Random Forest, optimizando hiperparámetros mediante validación cruzada.

### Parte 4, Regresión:
- Se desarrollaron modelos predictivos para estimar el precio de venta utilizando KNN y XGBoost, evaluando su desempeño tanto en entrenamiento como en test.


## Trabajo Práctico 2 : Propiedades en Venta

### Introducción

En el TP2 se dio continuidad al trabajo previo, aplicando nuevos modelos predictivos y técnicas avanzadas de ciencia de datos para profundizar el análisis de las propiedades en venta.

### Parte 1, Procesamiento del Lenguaje Natural (NLP):

- Se amplió el dataset original utilizando la columna de descripción de las propiedades para extraer nuevos aspectos de los anuncios, como “expensas” o “servicios incluidos”, aplicando técnicas de Minqing Hu y Bing Liu, Regex, y extracción de conocimiento de la Web (Open Information Extraction).
- Se entrenaron modelos de regresión XGBoost tanto con los hiperparámetros utilizados en el TP1 como con nuevos hiperparámetros optimizados, y se compararon los resultados obtenidos con y sin las nuevas columnas agregadas.

### Parte 2, Redes Neuronales:

- Se construyeron dos modelos de redes neuronales: uno para regresión y otro para clasificación. El modelo de regresión se utilizó para predecir el precio de las propiedades, optimizando la arquitectura para minimizar el error cuadrático medio (MSE). El modelo de clasificación predijo el atributo tipo_precio y se evaluó mediante precisión, recall y F1-Score.

### Parte 3, Ensamble de Modelos y Conclusiones:

- Se implementaron dos ensambles híbridos de modelos. El primero, un ensamble de tipo Voting, se aplicó al problema de clasificación, mientras que el segundo, un ensamble de tipo Stacking, combinó varios modelos de regresión para predecir el precio de las propiedades. Ambos ensambles fueron comparados con los modelos individuales utilizados en los puntos anteriores.
- Se discutieron los resultados obtenidos en las distintas etapas del trabajo, comparando el rendimiento de los modelos mejorados con los del TP1, y destacando las principales mejoras obtenidas. Además, se mencionaron algunas alternativas que no se exploraron debido a las limitaciones de tiempo y recursos.
