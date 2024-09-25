# ProyeccionSuperficieLago
Este repositorio contiene el código necesario para recopilar y procesar datos de la superficie de un lago (en km²) a través de imágenes satelitales. Se incluye la base de datos generada con estos datos (más datos climáticos recopilados) y un script que utiliza un modelo ARIMA para realizar proyecciones de la superficie del lago en el tiempo.


## Objetivos
El objetivo es analizar los cambios en la superficie del Lago Caburgua especificamente utilizando imágenes satelitales desde 1984 a 2022. Identificando los factores climaticos y antropicos que afectan a la superficie del lago, con el fin de realizar proyecciones futuras implementando un modelo ARIMA para predecir la superficie bajo distintos escenarios hasta el 2030.

## Recopilación de Datos:

En principio se usaron imágenes satelitales de Google Earth Time-lapse para estimar la superficie del lago. Se obtuvieron datos de variables climáticas como precipitaciones anuales, temperaturas máximas y fenómenos climáticos. Ademas, se consideró la construcción de un dique en el río Trafampulli el año 2007 como factor antrópico relevante.

## Análisis de Imágenes:

Se implementó el algoritmo de Clustering K-means (desde "Script Clustering/Aproximación_áreas.ipynb") para segmentar las áreas correspondientes al lago en las imágenes satelitales. Para obtener la superficie estimada del lago para cada año de estudio.

## Modelado Predictivo:

Se utilizó un modelo ARIMA (3,0,1) en RStudio para predecir la superficie del lago considerando variables climáticas y la presencia del dique.
Se plantearon dos escenarios futuros: uno con la reconstrucción del dique en 2026 y otro sin ella.


## Resultados
Se obtuvo una estimación confiable de la superficie del lago en función del tiempo mediante el algoritmo de Clustering K-means. Y el modelo ARIMA mostró un buen ajuste para la predicción de la superficie del lago hasta el año 2030, validado con una prueba de Ljung-Box.
Se identificó que la reconstrucción del dique podría generar una disminución mayor de la superficie del lago en comparación con el escenario de no intervención (ausencia del dique).


## Conclusiones:
El estudio evidencia la importancia de factores climáticos, y principalmente antrópicos en la variación de la superficie del Lago Caburgua. Las proyecciones sugieren que, sin eventos extremos no contemplados, la estabilidad de la superficie del lago podría mantenerse en el escenario de ausencia de intervenciones antrópicas como la reconstrucción del dique.

## Requisitos del Proyecto:
- Python (para el análisis de imágenes y Clustering K-means).
- RStudio (para el modelo ARIMA y análisis estadístico).
- Librerias de Python: numpy, pandas, sklearn.
- Librerias de R: forecast, tseries.
  

## Autores
Frugone R. - raul.frugone@alu.ucm.cl
Llanos A. - angel.llanos@alu.ucm.cl
Neira F. - felipe.neira@alu.ucm.cl
Huerta M.
Rodríguez M.

## Referencias
- Fundación Sustenta Pucón (2021). Informe Ejecutivo Nivel de Agua en Lago Caburgua.  https://www.sustentapucon.cl/wp-content/uploads/2021/12/INFORME-CABURGUA-SUSTENTABLE-3.pdf
- Bahamóndez Provoste, C. F. (2021). Cambio climático y su efecto sobre los cuerpos de agua de Chile Central: variación interanual superficial de los lagos andinos (32° S-36° S) entre 1984 y 2020. https://repositorio.uchile.cl/handle/2250/188022
- Servicio Nacional de Geología y Minería. (s.f.). Volcán Villarrica. https://rnvv.sernageomin.cl/volcan-villarrica/
- Instituto Nacional de Estadísticas de Chile. (2023). Estadísticas de Medio Ambiente.  https://stat.ine.cl/Index.aspx?DataSetCode=E10000001
- National Weather Service (2023). Cold \& Warm Episodes by Season.https://origin.cpc.ncep.noaa.gov/products/analysis\_monitoring/ensostuff/ONI\_v5.php
- Ozdemir, S., Yaqub, M., \& Yildirim, S. O. (2023). A systematic literature review on lake water level prediction models. Environmental Modelling \& Software, 163, 105684.
- Cryer, J. D., \& Chan, K. S. (2008). Time series regression models. Time series analysis: with applications in R
