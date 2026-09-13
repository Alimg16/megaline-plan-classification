# megaline-plan-classification
## Descripción

Proyecto de machine learning realizado para Megaline con el objetivo de recomendar a los usuarios uno de sus planes actuales: Smart o Ultra.

El modelo utiliza información sobre el comportamiento mensual de los clientes, como llamadas, minutos, mensajes y uso de Internet.

## Objetivo

Desarrollar un modelo de clasificación con una exactitud mínima de 0.75 para predecir el plan más adecuado para cada usuario.

## Tecnologías utilizadas

- Python
- pandas
- scikit-learn

## Metodología

1. Exploración y revisión inicial de los datos.
2. División de los datos en conjuntos de entrenamiento, validación y prueba.
3. Entrenamiento y comparación de:
   - Árbol de decisión
   - Bosque aleatorio
   - Regresión logística
4. Ajuste de hiperparámetros usando el conjunto de validación.
5. Evaluación del mejor modelo con el conjunto de prueba.
6. Prueba de cordura usando una estrategia de referencia.

## Resultados

Los mejores resultados en validación fueron:

- Árbol de decisión: accuracy de 0.8025
- Bosque aleatorio: accuracy de 0.8212
- Regresión logística: accuracy de 0.7185

El mejor modelo fue un bosque aleatorio con:

- `n_estimators = 40`
- `max_depth = 9`

En el conjunto de prueba obtuvo una exactitud de: 0.8087

Como prueba de cordura, una estrategia que siempre predice el plan Smart obtuvo una exactitud de 0.6936.

## Conclusión

El modelo de bosque aleatorio superó el umbral mínimo de 0.75 y también obtuvo mejores resultados que la estrategia de referencia. Por lo tanto, fue seleccionado como el modelo final para la tarea de clasificación.
