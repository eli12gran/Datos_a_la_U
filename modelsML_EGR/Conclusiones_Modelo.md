# **Conclusiones para modelo: Análisis de Correlación para Entender la Relación Entre Precios de Insumos y Exportaciones**

Observemos los resultados de los scores y las métricas tomadas en cuenta:

**Para la Regresión Lineal con Regularización de Ridge:**

```
**********Scores y resultados para Regularización de Ridge**********
Training set score: 0.20
Test set score: 0.21
Validation set score: 0.20

MSE para Ridge en el conjunto de prueba: 5.9454
RMSE para Ridge en el conjunto de prueba: 2.4383
MAPE para Ridge en el conjunto de prueba: 0.6659

```

**Para Random Forest:**

```
**********Scores y resultados para Random Forest**********
Training set score: 0.97
Test set score: 0.86
Validation set score: 0.86

MSE para Random Forest en el conjunto de prueba: 1.0562
RMSE para Random Forest en el conjunto de prueba: 1.0277
MAPE para Random Forest en el conjunto de prueba: 0.2360
R² para Random Forest en el conjunto de prueba: 0.8588

```

**Para AdaBoost:**

```
**********Scores y resultados para AdaBoost**********
Training set score: 0.80
Test set score: 0.80
Validation set score: 0.80

MSE para AdaBoost en el conjunto de prueba: 1.4918
RMSE para AdaBoost en el conjunto de prueba: 1.2214
MAPE para AdaBoost en el conjunto de prueba: 0.3521
R² para AdaBoost en el conjunto de prueba: 0.8006
```
De una forma más visual:

![Métricas del Modelo](../metricas_modelo_1.jpg)

Los resultados obtenidos respaldan nuestra hipótesis de que las técnicas de machine learning son necesarias para modelar de manera efectiva el impacto de los precios de los insumos agrícolas en las exportaciones de cultivos. La regresión lineal tradicional no fue capaz de capturar ni siquiera en un porcentaje mínimo las relaciones complejas y no lineales entre las variables, lo que llevó a un desempeño deficiente en comparación con los modelos más sofisticados.

Por otro lado, tanto Random Forest como AdaBoost mostraron un rendimiento significativamente mejor, lo que sugiere que estos modelos pueden identificar relaciones complejas entre los insumos y las exportaciones que no son evidentes a través de enfoques lineales. **Sin embargo, es importante subrayar que el objetivo no es tanto predecir de manera exacta el valor de las exportaciones, sino más bien identificar si existen relaciones significativas entre las variables y cómo esas relaciones se pueden modelar eficazmente con técnicas de machine learning.**

Este análisis demuestra que los modelos no lineales, como Random Forest y AdaBoost, son herramientas poderosas para descubrir patrones e interacciones más complejas entre las variables, lo que los hace particularmente útiles en este tipo de estudios económicos y agrícolas.
