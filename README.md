# Predicción de Accidentes Cerebrovasculares
En esta Notebook se busca predecir mediante algoritmos de Machine Learning si un individuo puede sufrir un Accidente Cerebrovascular basándose en las siguientes características:
 
* Edad
* Índice de masa corporal
* Nivel de glucosa en sangre
* Genero
* Si el paciente es hipertenso
* Si el paciente esta casado
* Si el paciente es fumador
* tipo de trabajo
* lugar de residencia
* id
* Si el paciente presenta enfermedades al corazón

## Entendiendo los datos
Para poder entender los datos, se graficaron todas las características y luego se procedió a realizar una matriz de correlación para entender cuales son las variables que determinan mas fuertemente el resultado respecto a la posibilidad de padecer un ACV.  

## Pre procesamiento de datos
Debido a que el conjunto de datos presenta valores atípicos y características categóricas, fue necesario realizar un pre procesamiento de datos para facilitar la utilización de los mismos en los modelos de Machine Learning.

## Sobremuestreo
Ya que el dataset presenta muy pocos datos de pacientes que padecieron ACV se procedió a realizar un sobremuestreo para equilibrar la cantidad y que los algoritmos puedan captar mejor las características, en este caso se utilizo la técnica de sobremuestreo SMOTE

## Machine Learning
Debido a que el objetivo es lograr predecir si el paciente tendrá o no ACV se utilizaran técnicas de Regresión de entrenamiento supervisado.
Los algoritmos utilizados fueron:
* Regresión Logística
* Random Forest
* XGBoost
* KNN
* Redes Neuronales
* Árbol de Decisión

Para intentar lograr la una buena performance posible se utilizo GridSearch en busca de las mejores características para cada modelo.

## Evaluación 
Para evaluar a los distintos modelos, utilizaremos la métrica de Sensibilidad, ya que considero que la importancia reside en evaluar los verdaderos positivos en función del total de valores positivos.
Por otro lado también se utilizara como métrica el valor AUC

## Conclusiones
Luego de la evaluación de todos los modelos, los resultados frente al test set son los siguientes:

![image](https://user-images.githubusercontent.com/30410928/131046235-1861dcca-4e3d-4bb5-82fe-2f30a0c18306.png)

El modelo que obtuvo mejor resultado fue la red neuronal, seguido por la regresión logística con ambos por encima del 80% en Sensibilidad y mas del 75% en AUC 

