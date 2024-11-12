Los resultados más importantes a destacar para el EDA sobre la producción y el rendimiento de la actividad agropecuaria se describen a continuación. Estos se obtuvieron con base en las visualizaciones y todo el análisis desarrollado en el documento
[`EDA_cultivos.ipynb`](https://github.com/eli12gran/Datos_a_la_U/blob/main/EDAs/EDA_cultivos.ipynb). Si desea ir directamente a los gráficos interactivos puede ingresar [aquí](https://colab.research.google.com/drive/1uwoA4n3wOl78dCpV1AUQycdQWNr2Ou_C?usp=sharing).

- En primer lugar, al ver estadísticas relacionadas con la producción (es decir, la cantidad de toneladas cosechadas), se observa que la producción de caña es considerablemente superior al resto de los cultivos registrados en el conjunto de datos.

### Tendencias temporales para cada grupo de cultivo:

Las gráficas que muestran el área sembrada y área cultivada por año para cada grupo de cultivo nos indican relaciones importantes. En primer lugar, se observa que en 2021 y 2022 hubo una disminución en estas áreas, por lo que es relevante considerar qué situaciones pueden haber causado esto, como fenómenos climáticos o situaciones políticas.

Otro grupo de cultivos que tuvo un declive en el área sembrada y cosechada fueron los cultivos para condimentos, bebidas medicinales y aromáticas, que desde 2021 tuvieron una gran disminución en comparación con 2020 y 2019, luego para 2022 y 2023 aumentó un poco pero siguen siendo menores que los primeros dos años estudiados.

Similarmente para los cultivos de leguminosas, estos han venido decayendo en los a medida que pasan los años, sin indicios de algún cambio de tendencia.

En cuanto a los cultivos tropicales tradicionales, estos parecen mantenerse muy estables durante los años registrados, lo cual es positivo puesto que la mayor producción está concentrada aquí. De igual forma sucede para cultivos de oleaginosas.

Un caso especial son los cultivos de raíces y tubérculos, los cuales, al observar el área sembrada parecen ser estables e incluso en 2023 muestran un aumento, pero el área cosechada cada vez difiere más en comparación con el área sembrada, lo que puede llegar a indicar fenómenos que afectan estos tipos de cultivos entre las épocas de siembra y cosecha, lo que da lugar a la pérdida de área cosechada superior a lo que suele esperarse, traduciéndose en pérdidas para los productores.

Finalmente, para cultivos frutales, se ha visto un panorama productivo puesto que las áreas sembradas y cosechadas han aumentado consecutivamente.



- También se realizó un gráfico de dispersión para identificar qué tipo de relación hay entre pares de variables. Específicamente se decidió graficar Área sembrada vs Área cosechada, la cual mostró una tendencia lineal, como podría esperarse, aunque hay algunos datos que parecen atípicos y es importante estudiar más a profundidad. También se graficó Área sembrada vs Producción y Área cosechada vs Producción, las cuales presentan una tendencia más compleja, que se cree que es debido a la alta producción que se obtiene por área sembrada y cosechada en los cultivos de caña, lo cual da esa aparente doble tendencia y genera la oportunidad de explorar más a fondo estas relaciones complejas por medio de modelos de Machine Learning.
