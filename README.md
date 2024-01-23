# Proyecto de Predicción de precios de renta de alojamientos turísticos en Barcelona
Este repositorio contiene un proceso desde 0 hasta la creación de un modelo de predicción de valores de renta para alojamientos turísticos en la ciudad de Barcelona, España, considerando como alojamiento aquellos inmuebles que pertenecen a casas o apartamentos completos y habitaciones privadas con el fin de generar una herramienta de apoyo para tomar las mejores decisiones a la hora de rentar u ofrecer una propiedad.


## Abstract
Cada año que pasa, las personas tienen más posibilidades de viajar a otros países y uno de los más atractivos para los países sudamericanos es España, principalmente por el idioma. España se caracteriza por tener ciudades muy turísticas en el verano europeo, como Barcelona, Madrid, la isla de Mallorca, entre otras. Existen muchas aplicaciones para alojar en distintas ciudades del mundo, dentro de las cuales su precio depende de muchos factores, como cercanía a atractivos turísticos, los servicios que ofrecen, la capacidad de personas admitidas, etc. Este proyecto busca generar un modelo que permita estimar el precio de renta de alojamientos turísticos, ya sea de una habitación privada o de la renta de una casa/apartamento en la ciudad de Barcelona, comprendiendo las relaciones entre las características de los alojamientos y sus respectivas rentas, con el fin de ayudar a los anfitriones a ajustar sus valores de renta y a los que quieran incursionar en esta área de arrendar alojamientos turísticos tomando la mejor decisión. Para este proyecto se cuenta con la hipótesis nula (H0) de que no existe una relación entre las características del alojamiento con el precio de este. Por el contrario, la hipótesis de investigación (H1) sugiere que si existe una relación entre las características de un alojamiento y su precio de renta. Las hipótesis de interés para esta entrega son:

* Existe una correlación positiva entre el número de personas admitidas y el precio
* Existe una correlación positiva entre el número de dormitorios y el precio del alojamiento

## Objetivo
El objetivo principal del proyecto es estimar precios de renta de alojamientos turísticos en Barcelona, España, estando dentro de los rangos de valores más comunes, es decir, sin ser excesivamente costoso ni excesivamente barato.

## Algoritmo propuesto
Antes de aplicar distintos modelos de Machine Learning, además del dataset final se construyeron 2 más, uno con las variables transformadas a su raíz cuadrada y otro con las variables transformadas a su logaritmo. Con estos 3 conjuntos de datos, mediante distintos modelos de Machine Learning y gracias a LazyPredict se obtuvo que los mejores modelos para estos 3 dataset fueron Regresión lineal para los 2 conjuntos transformados y LassoLars para el dataset original. 

Al analizar las métricas de regresion (r2 y RMSE) de los 3 modelos, se concluye que los 2 mejores son las regresiones lineales, por lo que se mejoran mediante ColumnTransformer y GridSearchCV utilizando como hiperparametros los grados del polinomio. 

De esta manera, se compararon estos 2 modelos de regresión lineal obteniendo como el mejor de todos la Regresión Lineal para el conjunto de datos con las variables transformadas a su raíz cuadrada con un r2 de 0.59 y un RMSE de 31.7 euros. 
<br><br><br>

# Instrucciones de Uso

1. Antes que todo, se debe ejecutar solamente el código ubicado en el encabezado "Librería a instalar", el cual contiene una librería de skimpy. 

2. Reiniciar el entorno, ya que es necesario para continuar con los otros encabezados.

3. Ejecutar el resto de los códigos de cada encabezado (omitiendo "Librería a instalar")

