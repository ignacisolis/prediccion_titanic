# Predicción de la supervivencia en el accidente del titanic
### Problematica 
Es bien sabido que en el accidente del titanic las mujeres y los niños eran los que tenian mayor probabilidades de salvarse, pero después de ellos ¿quienes le siguen?

### Aplicaciones y algoritmos 
A través del lenguaje de programación de python se realizó un analisis de datos para ver qué variables pueden estar involucradas para saber quien se puede salvar de este accidente
para esto se utilizó pandas, maptplotlib y seaborn con la finalidad de analizar y comprender cuales eran las variables que estaban estrechamente relacionadas con la supervivencia.

### Aprendizaje 
Através de la biblioteca de skitlearn se opto por utilizar la regresion logistica en primera instancia, una vez se comprueba que no es el mejor modelo (dado a que los resultados no eran muy satisfactorios) 
se decantó por utilizar randomforest por su capacidad de capturar relaciones no lineales.

Finalmente se concluye que a pesar de no tener un buen set de datos se logro implementar un algoritmo con hiperparametros lo suficientemente correctos para poder tener un aprendizaje correcto
encontrando una presicion del 70%, una  exactitud del 76%, f1_score del 61% y 
