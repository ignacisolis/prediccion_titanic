# Predicción de la supervivencia en el accidente del Titanic

## Problemática

Es bien sabido que en el accidente del Titanic las mujeres y los niños eran quienes tenían mayores probabilidades de salvarse. Pero, después de ellos, ¿quiénes le siguen? Este proyecto busca identificar qué otras variables influyeron en la supervivencia de los pasajeros.

## Análisis de datos

A través del lenguaje de programación Python se realizó un análisis exploratorio de datos para identificar qué variables podían estar relacionadas con la supervivencia de los pasajeros. Para esto se utilizaron las bibliotecas **pandas**, **matplotlib** y **seaborn**, con la finalidad de analizar y comprender cuáles eran las variables más estrechamente relacionadas con la supervivencia.

## Aprendizaje automático

A través de la biblioteca **scikit-learn** se optó, en primera instancia, por utilizar regresión logística. Al comprobar que no era el mejor modelo (los resultados no eran del todo satisfactorios), se decidió utilizar **Random Forest**, por su capacidad de capturar relaciones no lineales entre las variables.

Para mejorar el desempeño del modelo se implementaron las siguientes técnicas:

- **Ingeniería de variables**
- **Balanceo de clases**: uso de `class_weight='balanced'` en el Random Forest para compensar el desbalance entre sobrevivientes y no sobrevivientes.
- **Optimización de hiperparámetros**: búsqueda de los mejores parámetros (`n_estimators`, `max_depth`, `min_samples_leaf`, entre otros) mediante `GridSearchCV`/`RandomizedSearchCV`.

## Conclusión

A pesar de no contar con un conjunto de datos ideal, se logró implementar un algoritmo con hiperparámetros lo suficientemente ajustados como para obtener un aprendizaje adecuado. Los resultados finales del modelo de Random Forest fueron:

| Métrica | Valor |
|---|---|
| Exactitud (Accuracy) | 74% |
| Precisión (Precision) | 50% |
| Sensibilidad (Recall) | 77% |
| Puntaje F1 (F1-score) | 61% |

Estos resultados indican que el modelo identifica correctamente a la mayoría de los sobrevivientes reales (alta sensibilidad), aunque a costa de generar cierta cantidad de falsos positivos (precisión más moderada), un comportamiento esperable dado el desbalance de clases presente en el dataset del Titanic.
