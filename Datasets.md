# **Información y localización de los Datasets usados**

En este documento encontrarán la descripción de cada uno de los datasets que se han usado hasta ahora para la elaboración del estudio que se está llevando a cabo en nuestro proyecto. En este punto es importante recordar que nuestro objetivo es encontrar patrones, tendencias y oportunidades en el sector agrícola a partir de los datos abiertos y con esto poder generar estrategias que el gobiernos y otros actores pueden utilizar para crear iniciativas de apoyo. Para lograr esto, **hemos seleccionado 7 bases de datos** que nos permitirán entender la financiación a los agricultores, el uso del suelo para plantaciones comerciales, las fluctuaciones de costos en los insumos agrícolas, importaciones y exportaciones agrícolas y las características y productividad de este sector. Con este fin entonces hemos seleccionado diversas bases de datos de diversas fuentes.

## **Bases de datos seleccionadas de las disponibles en la [página del concurso](https://www.datos.gov.co/Ciencia-Tecnolog-a-e-Innovaci-n/Conjunto-de-datos-concurso-Datos-a-la-U-2024/bbf6-qe46/about_data):**

1. **[Exportaciones agrícolas no tradicionales y tradicionales](https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Exportaciones-agr-colas-no-tradicionales-y-tradici/h7mi-sbxb/about_data)**: El indicador mide el valor en dólares de las exportaciones agropecuarias no tradicionales y tradicionales.
 
2. **[Índice de precios de insumos agrícolas](https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/-ndice-de-precios-de-insumos-agr-colas/gwbi-fnzs/about_data)**: Índice que resume el comportamiento de los precios a nivel nacional, de los productos más utilizados en la actividad agrícola para las diferentes etapas de producción, en productos: fertilizantes, entre simples y compuestos; plaguicidas entre herbicidas, fungicidas e insecticidas y; otros insumos entre coadyuvantes, reguladores fisiológicos y molusquicidas

3. **[Base de datos relacionada con área plantada con Plantaciones Forestales Comerciales](https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Base-de-datos-relacionada-con-rea-plantada-con-Pla/h3uz-jvkj/about_data)**: La base de datos contiene los registros administrativos de las áreas establecidas con plantaciones con fines comerciales en todo el territorio nacional a nivel departamental.

## **Bases de datos seleccionadas de las disponibles en la página de [Datos Abiertos](https://www.datos.gov.co/browse?category=Agricultura+y+Desarrollo+Rural&sortBy=newest&utf8=%E2%9C%93)**

1. **[Colocaciones de Crédito Sector Agropecuario - 2021- 2024](https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Colocaciones-de-Cr-dito-Sector-Agropecuario-2021-2/w3uf-w9ey/about_data)** : Operaciones de crédito colocadas en el sector agropecuario 2021 - 2024

2. **[Evaluaciones Agropecuarias Municipales – EVA. 2019 - 2023. Base Agrícola](https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Evaluaciones-Agropecuarias-Municipales-EVA-2019-20/uejq-wxrr/about_data)**

## **Bases de datos seleccionadas del [Observatorio de Desarrollo Económico](https://observatorio.desarrolloeconomico.gov.co/)**

1. **[Bases de datos de exportaciones](https://observatorio.desarrolloeconomico.gov.co/temas/exportaciones/bases)**

2. **[Bases de datos de importaciones](https://observatorio.desarrolloeconomico.gov.co/temas/importaciones/bases)**

Para esta parte específica es importante aclarar cuáles fueron exactamente las bases de datos que utilizamos para las exportaciones e importaciones. Cuando se vaya al link de cada una de las bases de datos, se podrá observar que cada una de éstas se encuentra por año y separadas. Con el fin de tener una base de datos con suficientes datos y con información suficientemente significativa, decidimos entonces **juntar las bases de datos de importaciones y exportaciones de los años 2018-2024 que allí se encuentran**. Así pues el dataset final para cada una fue construido con:

> **Para exportaciones:**

	`BD exportaciones 2018`
	`BD exportaciones 2019`
	`BD exportaciones 2020`
	`BD exportaciones 2021`
	`BD exportaciones 2022`
	`BD exportaciones 2023`
	`BD exportaciones 2024` (Agosto 2024)

> **Para las importaciones:**

	`BD importaciones 2018`
	`BD importaciones 2019`
	`BD importaciones 2020`
	`BD importaciones 2021`
	`BD importaciones 2022`
	`BD importaciones 2023`
	`BD importaciones 2024` (Agosto 2024)

Éstas bases de datos armadas de esta forma fueron nombradas: `exportations_2018_2024_complete.csv`, `importations_2018_2024_complete.csv`.

Debido al gran tamaño de los datasets, estos no se incluyen en GitHub. En su lugar, hemos proporcionado un enlace a una carpeta de Google Drive donde podrán descargarlos. Los datasets se encuentran en dicha carpeta y se llaman:

El link de la carpeta de Google Drive se encuentra [acá](https://drive.google.com/drive/folders/1v_IgWjiG-QZhkPw8DvTxctiA1GUS_y0K?usp=sharing)
