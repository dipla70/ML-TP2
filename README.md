# ML-TP2 Problem Set 2: Machine Learning 2024

Descripción del Proyecto

Este proyecto tiene como objetivo predecir la pobreza en hogares colombianos utilizando técnicas de Machine Learning. Se implementan y comparan distintos modelos de predicción para abordar el problema como una tarea de clasificación binaria, donde 0 indica que el hogar no es pobre y 1 que sí lo es.

Los modelos principales utilizados incluyen:
	•	Lasso y ElasticNet (Regresión Regularizada)
	•	Árboles de Decisión (CART)
	•	Random Forest (con bagging)
	•	Adaboost (Boosting)
	•	Regresión Logística (Logit)

El desempeño de cada modelo se evalúa utilizando F1-Score como métrica principal, ya que equilibra la precisión y exhaustividad en un problema de clasificación.

Estructura del Proyecto
	•	problem_set2.ipynb: Script principal que contiene el análisis completo, procesamiento de datos, entrenamiento y evaluación de los modelos.
	•	data/: Directorio con los datos utilizados en el estudio (microdatos del DANE) en formato zip.
	•	results/: Contiene resultados en un csv por cada predicción
 
Instalación

Clonar este repositorio y ejecutar el script con un entorno configurado con las siguientes librerías:

pip install numpy pandas scikit-learn matplotlib seaborn imbalanced-learn

Librerías Utilizadas
	•	pandas y numpy: Manipulación y procesamiento de datos.
	•	scikit-learn: Entrenamiento y evaluación de modelos de Machine Learning.
	•	matplotlib y seaborn: Visualización de datos.
	•	imbalanced-learn: Balanceo de clases en los datos.

Metodología
	1.	Procesamiento de Datos:
	•	Imputación de valores faltantes.
	•	Transformación de variables relevantes de las bases de hogares e individuos.
	•	Creación de variables adicionales (e.g., proporción de personas ocupadas, recepción de subsidios).
	2.	Modelos Utilizados:
Se entrenaron los siguientes modelos utilizando validación cruzada K-Fold y optimización de hiperparámetros con Grid Search y Randomized Search:
	•	Lasso
	•	ElasticNet
	•	Árboles de Decisión (CART)
	•	Random Forest
	•	Adaboost
	•	Logit (Regresión Logística)

Comparación de Modelos

El desempeño de los modelos se evaluó utilizando el F1-Score. En la evaluación inicial:
	•	Random Forest mostró el mejor rendimiento en Kaggle, aunque los resultados difirieron ligeramente de los obtenidos localmente.
	•	Lasso y ElasticNet también presentaron un buen desempeño.

Ejecución del Script

Ejecutar el script principal problem_set2.ipynb paso a paso en un entorno como Jupyter Notebook o Google Colab.

Resultados Principales

Desempeño del Modelo Random Forest:
	•	F1-Score en Kaggle: 0.54

Importancia de las Variables:
Las variables más relevantes según el modelo Random Forest incluyen:
	1.	Monto de alquiler (monto_alq)
	2.	Proporción de personas ocupadas (prop_ocup)
	3.	Proporción de hombres (prop_sexo)
	4.	Número de cuartos (n_cuartos)

Autores
	•	Ara Francisco
	•	Corradi Valentín
	•	Di Placido Pedro

Referencias
	•	DANE Colombia: Datos de la encuesta “Medición de Pobreza Monetaria y Desigualdad 2018”.
	•	Modelos implementados con base en las clases de Machine Learning de la Maestría en Economía - UNLP.

Repositorio público: https://github.com/dipla70/ML-TP2.git
