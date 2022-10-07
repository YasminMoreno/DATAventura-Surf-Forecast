# DATAventura-Surf-Forecast

![portada](https://github.com/YasminMoreno/DATAventura-Surf-Forecast/blob/main/img/portada_proyecto_final.png)

## Proyecto final - Bootcamp Ironhack - FT Agosto 2022

Herramienta de predicción de olas para hacer surf según las condiciones meteorológicas (utilizando machine learning) que permite clasificarlas por horas para los diferentes niveles de habilidad de los surfistas.


## Objetivo

Realizar el proyecto final del Bootcamp utilizando todo lo aprendido durante estas 9 semanas.

## Pasos

1. Encontrar la API desde la cual extraeremos los datos.
2. Una vez encontrada la API, utilizamos la librería geopy para completar directamente parte de la formula de la API con la latitud y longitud de la ubicación que queremos, para descargarnos los datos históricos meteorológicos del mar.
3. Abrimos el JSON descargado de la API con json_normalize.
4. Juntamos todos los csv de los históricos y lo limpiamos con Pandas.
5. Pasamos la columna time que es de tipo object a datetime y posteriromente le quitamos la zona UTM.
6. Utilizamos la librería Prophet para hacer Machine Learning y así predecir de cada columna los datos futuros.
7. Juntamos cada columna que nos da Prophet entre ellas y posteriormente con el csv del historico desde el último dato que tenemos actualizado.
8. Creamos los grupos por niveles y valoraciones de las olas del día y hora para poder surfear. También pasamos la columna de dirección del viento en grados azimutales a coordenadas en letras.
9. Cargamos el csv directamente en Tableu ya que de momento solo tenemos una tabla. Cuando creemos una tabla por cada playa lo pasaremos a SQL primero.
10. Realizamos diferentes gráficos con Tableau. Gráficos interactivos y gráficos con nuevos iconos personalizados descargados desde la web flaticon y adjuntados a la carpeta de formas de nuestro directorio de Tableau para poderlos utilizar.
11. Por último hacemos la ppt final en Keynote.

## Entregables

1. Archivo `apisurf.ipynb` donde esta el código para descargarnos las columnas de la API. 
2. Archivo `Presentacion_Proyecto_Final.pdf`  pdf de la presentación de Keynote. 
3. Archivo `Tableau_Proyecto_Final.pdf` pdf de los gráficos de Tableau desktop. 
4. Carpeta `data` con todos los CSV del histórico por fechas, el archivo con la plantilla de machine learning utilizada, el archivo `Proyecto_final.ipynb` con todo el código utilizado tras descargar los JSON y pasarlos a CSV y el archivo `surf_proyect_final.csv` con el CSV final para exportarlo a Tableau.

## Conclusiones

- Los mejores meses para surfear en un nivel intermedio o avanzado son de enero a marzo, mientras que algunos días de los demás meses podríamos también con un nivel principiante.
- Utilizando Machine Learning Prophet nos da un resultado con poco margen de error, sobre todo en algunas columnas como la del tiempo y las más necesarías para nuestro estudio. 
