# **Cultivando Conexiones: Estudio Integrado de las Dinámicas del Panorama Agrícola en Colombia**

#### ***Autoras de la idea: Elizabeth Granda Rodríguez, Valentina Miranda Garcés***
#### ***Facultad de Ciencias Básicas, Computación Científica, Universidad de Medellín***

![Logos de GitHub](logos_github.jpg)


En el presente repositorio se presenta la idea de proyecto para el concurso Datos a la U. Participamos en la categoría de **Agricultura y Desarrollo Rural** con el proyecto que titula este documento: *Cultivando Conexiones: Estudio Integrado de las Dinámicas del Panorama Agrícola en Colombia*. 

El sector agrícola global y colombiano se enfrenta a una serie de desafíos complejos, como la variabilidad climática, la falta de diversificación de cultivos y el limitado acceso a tecnologías y financiamiento. Estas dificultades no solo afectan la productividad y competitividad de los agricultores, sino que también ponen en riesgo la seguridad alimentaria y la economía de nuestros países.

Reconocemos la importancia vital del sector agrícola para nuestra sociedad y creemos que es nuestro deber contribuir a su desarrollo. Como estudiantes de Computación Científica, hemos adquirido sólidas bases en matemáticas, computación y estadística, herramientas que nos permiten analizar y ver los datos desde diferentes perspectivas para así desarrollar soluciones innovadoras. Motivadas por esta problemática y por las herramientas a nuestro alcance, proponemos aplicar nuestros conocimientos para diseñar soluciones tecnológicas que aborden los desafíos específicos del sector agrícola colombiano. Creemos que, al hacerlo, no solo estaremos contribuyendo al progreso económico del país, sino también garantizando la sostenibilidad de un sector que sustenta a millones de personas.

**Objetivo:** Utilizar técnicas de Machine Learning para analizar datos abiertos del sector agrícola colombiano y generar diversos modelos capaces de identificar patrones complejos y tendencias emergentes. Esta información busca poder ser de utilidad para el diseño de recomendaciones estratégicas que permitan a los tomadores de decisiones diseñar políticas públicas y programas de apoyo más efectivos, dirigidos a mejorar la productividad, la sostenibilidad y la competitividad del sector agrícola colombiano, con un enfoque especial en la identificación de los productores más vulnerables y las regiones con mayor potencial de crecimiento.


Para lograr este acometido se hará uso de las bases de datos que provee el concurso en su [página web](https://www.datos.gov.co/Ciencia-Tecnolog-a-e-Innovaci-n/Conjunto-de-datos-concurso-Datos-a-la-U-2024/bbf6-qe46/about_data) además de otras fuentes como el [Observatorio de Desarrollo Económico](https://observatorio.desarrolloeconomico.gov.co/) y también otras bases disponibles en la [página de Datos Abiertos](https://www.datos.gov.co/browse?sortBy=newest&utf8=%E2%9C%93). La especificación de cada una de las bases de datos a usar se encuentra en el archivo `Datasets.md`.  Es importante aclarar que se desea expandir más el horizonte de la idea de forma que se puedan abarcar más contextos e identificar soluciones potenciales a otras problemáticas que afectan al sector agricultor en Colombia.

---
## **Requerimientos Tecnológicos**

Para garantizar la replicabilidad del proyecto, a continuación, se describen los recursos tecnológicos necesarios para ejecutar el código, escrito en Python, y las librerías empleadas en el desarrollo de cada paso documentado. Documentamos en esta parte los paquetes requeridos con las versiones que se usaron de cada uno de ellos. Recomendamos realizar un update de las librerías y de Python cuando se realice la clonación del repositorio con el fin de evitar problemas de versiones y todo el programa pueda correr de forma correcta.

* Versión de Python: `3.9.8` o superior 

* Paquetes requeridos:
	* `Pandas` (versión `2.1.4` o superior)
	* `numpy` (versión `1.25.0` o superior)
	* `matplotlib`(versión `3.4.3` o superior)
	* `seaborn` (versión `0.13.2` o superior)
	* `plotly` (versión `5.18.1` o superior)
	* `sklearn` (versión `1.5.2` o superior)

En caso de que se desee hacer la instalación de un paquete individual porque no cuenta con él en su máquina local, puede hacerlo utilizando `pip` de la siguiente forma:

```
pip install package_name
```

Y si desea instalar el programa con una versión específica:

```
pip install package_name==0.0.0
```

Donde el `0.0.0` será la versión que desee.

El paquete por excelencia para realizar estudios con herramientas de Machine Learning es el último mencionado en el listado anterior, es decir, `scikit-learn`. Con este paquete se lleva a cabo toda la creación e implementación del modelo, desde el preprocesamiento de los datos hasta la creación de nuevas columnas mediante *feature engineering*. `scikit-learn` incluye módulos para realizar Machine Learning supervisado y no supervisado, proporcionando todos los modelos necesarios para abordar problemas de regresión o clasificación, según lo requiera el proyecto.

---
## **Metodología**

### 1. Selección de las bases de datos

Las bases de datos fueron seleccionadas después de haber hecho una búsqueda exhaustiva de documentos, informes y reportes oficiales que brindan un panorama general sobre las necesidades del sector agrícola, y de acuerdo a esto fue posible identificar los conjuntos de datos con potencial para ofrecer información clave que permita llevar a abordar las necesidades que han sido planteadas en estas publicaciones:

- [Análisis Comparativo de Sistemas de Innovación Agropecuaria: Un abordaje hacia las mejores prácticas para Colombia](http://hdl.handle.net/20.500.12324/40195)
- [Generación de conocimiento para el sector agropecuario desde AGROSAVIA 2023](http://hdl.handle.net/20.500.12324/39006)
- [AGROSAVIA y su compromiso con el pequeño productor, la agricultura campesina, familiar y comunitaria](http://hdl.handle.net/20.500.12324/37360)
- [Balance social 2023](http://hdl.handle.net/20.500.12324/39036)
- [OECD (2022), Rural Policy Review of Colombia 2022](https://doi.org/10.1787/c26abeb4-en)

### 2. Análisis Exploratorio de los Datos (EDA)

Antes de realizar cualquier modelo de predicción o de tomar cualquier decisión crucial sobre qué hacer en el modelo, cómo implementarlo, qué modelo utilizar, etc, se debe hacer lo que se conoce como **Análisis Exploratorio de Datos**, más conocido como EDA (Exploratory Data Analysis) el cual es una fase crucial en cualquier proyecto de ciencia de datos o análisis, ya que establece una comprensión profunda y estructurada del conjunto de datos. Esta parte es esencial para saber qué información está disponible y cómo puede utilizarse. Permite identificar valores atípicos, datos faltantes o errores en los datos, como inconsistencias o duplicados, que pueden sesgar los resultados y afectar el rendimiento de los modelos. Al identificar estos problemas, se pueden realizar las correcciones necesarias antes de avanzar. Una de las razones más importantes por las cuales el EDA debe hacerse con minuciosidad es que acá se pueden explorar relaciones entre variables y se pueden detectar patrones interesantes, como correlaciones entre variables, que podrían ser útiles para el modelo predictivo o análisis, lo que por ende **ayuda a verificar o refutar hipótesis iniciales y a plantear nuevas hipótesis**. 

La parte del EDA es para las creadoras de la idea, la parte más importante de todas. Es por eso que para las 7 bases de datos que se han usado hasta el momento, se han realizado EDA´s individuales que recorren casi la totalidad de las columnas de cada dataset y se detallan las relaciones entre variables e identificación de diversos patrones que pueden ser útiles para la creación de nuevas features que llevarán a una buena implementación del modelo.

### 3. Resultados y conclusiones de los EDAs


### 4. Elección de los Modelos de Machine Learning

Con el fin de encontrar los patrones y las tendencias ocultas que creemos están en las bases de datos y en la relación de unas con otras, decidimos entonces llevar a cabo la implementación de modelos de machine learning que nos permitan relacionar las bases de datos entre sí. 

Existe una percepción errónea común por parte de algunos miembros de las comunidades de machine learning de que los modelos pueden explicar completamente un fenómeno sin la necesidad de un profundo conocimiento del contexto. En este punto es importante recordar que el machine learning es un *aprendizaje de máquina*, que no conoce de contextos sociales, políticos, culturales o económicos, y que, al ser humanos como somos, son los aspectos que conforman y erigen el mundo que nos rodea.


### 5. Interpretación de los Modelos de Machine Learning

### 6. Integración de los EDAs y los Modelos

Con el fin de encontrar los patrones y las tendencias ocultas que creemos están en las bases de datos y en la relación de unas con otras, decidimos entonces llevar a cabo la implementación de modelos de machine learning que nos permitan relacionar las bases de datos entre sí. 

Existe una percepción errónea común por parte de algunos miembros de las comunidades de machine learning de que los modelos pueden explicar completamente un fenómeno sin la necesidad de un profundo conocimiento del contexto. En este punto es importante recordar que el machine learning es un *aprendizaje de máquina*, que no conoce de contextos sociales, políticos, culturales o económicos, y que, al ser humanos como somos, son los aspectos que conforman y erigen el mundo que nos rodea.

---

### **Construcción del EDA**

Para la construcción de alkjdaksjdklsadj


## **Fuentes de Información**

## Alcance del proyecto y futuras oportunidades

El mundo de los datos no tiene límites, y esperamos que con este proyecto sea posible abrir el camino para muchas otras propuestas que complementen desde diferentes frentes el objetivo general que comprende aportar al crecimiento del sector agrícola en Colombia. 
