# Son las personas de la tercera edad los que presentaron mayor fatalidad en los accidentes de tránsito durante el año 2018 en Bogotá.
### Las personas de la tercera edad (Mayores de 60 años) son las que presentan el mayor indice de fatalidad en los accidentes de transito que se presentaron en el año 2018 en Bogotá, siendo el rango entre 71-80 años con 40 muertes el que aporta la mayor cantidad, seguido de los mayores de 81 años con 36 muertes y de 61-70 años con 34 muertes, siendo la incidencia por atropellamiento superior al 95% para cada uno de estos rangos.
Producto de accidentes de tránsito en la ciudad de Bogotá durante el año 2018 se presentaron 9861 victimas, dentro de las que se encuentran personas fallecidas, hospitalizadas o con algún grado de valoración médica. Estas son cifras que se obtuvieron gracias a la carga de datos que hizo la Secretaría de Movilidad de Bogotá por medio de la plataforma de Datos Abiertos Bogotá. Para lograr un mejor entendimiento de las incidendencias con victimas por accidentes de tráfico en la ciudad, se desarrollo la presente visualización en la cual se segmenta por rango de edades y causa de accidente los tres niveles de gravedad de las victimas que corresponden a victimas muertas, hospitalizadas y con valoración médica.
### Fuente: Datos Abiertos Bogotá </br> Accidentes de Tránsito en la ciudad de Bogotá - 2018 y diccionario de datos. </br> http://datosabiertos.bogota.gov.co/dataset/9af693ae-7051-43a3-90fa-1717a15c4890?_external=True
Los datos descargados de la fuente de Datos Abiertos Bogotá fueron preparados para construir tres tablas multivariadas (victimas muertas, hospitalizadas y valoradas), y adicional se definieron unos rangos de edades para cuantificar la cantidad de victimas según su gravedad:</br>Rango de edades: 
* Menor o igual a 4 años: Niños pequeños.
* 5-15 años: Niños y adolescentes.
* 16-23 años: Adultos jovenes.
* 24-30 años.
* 31-40 años.
* 41-50 años.
* 51-60 años.
* 61-70 años: Tercera edad.
* 71-80 años: Tercera edad.
* 81 años o más: Tercera edad.
El desarrollo de preparación de datos se hizo con el siguiente notebook (Jupyter):</br>https://github.com/hpuentes/victimas-trafico-bogota-2018/blob/master/Merge%20accidents.ipynb
</br></br>Diccionario de datos: https://github.com/hpuentes/victimas-trafico-bogota-2018/blob/master/Descripcion_variables_-_Accidentes_de_Tr_nsito.pdf
## Tarea Principal.
T1. Comparar la cantidad de victimas por rango de edad.</br>(Compare)-(Distribution)
### Tareas secundarias.
T2. Comparar la cantidad de victimas por tipo de accidente en un rango de edad.</br>(Compare)-(Distribution)
T3. Buscar por tipo de victima como es la distribución por edad de la cantidad y tipos de accidentes.</br>(Lookup)-(Distribution)
## WHAT?
### Attributes: 
* Rango edad: Ordered, Ordinal.
* Choque: Quantitative, Sequential.
* Atropello: Quantitative, Sequential.
* Caida de ocupante: Quantitative, Sequential.
* Volcamiento: Quantitative, Sequential.
* Otra causa: Quantitative, Sequential.
* Gravedad victima: Categorical.
### Dataset:
* Multidimensional table
## WHY?
1. Comparar la cantidad de victimas por rango de edad.</br>(Compare)-(Distribution)
2. Comparar la cantidad de victimas por tipo de accidente en un rango de edad.</br>(Compare)-(Distribution).
3. Buscar por gravedad de victima como es la distribución por edad de la cantidad y tipos de accidentes.</br>(Lookup)-(Distribution)
## HOW?
* Separate - Orden - Align: Barras de Rango de edades y tipo de accidente.
* Select: Selecciona gravedad de victima para actualizar distribución, selecciona cada fragmento de barra (Tipo de accidente en un rango de edad) para obtener detalles.
* Embed: Por cada barra de rango de edad se fragmenta por tipo de accidente.
### Channels:
* HUE: Colores para cada tipo de accidente.
* Position on common scale: Fragmentos de barra (Tipo de accidente en un rango de edad) con tamaño por tipo de incidente.
* Tilt: Barras verticales para cada rango de edad indicando cantidad de incidentes.
## Distribución por rango de edad y causa de incidente de las victimas en accidentes de tránsito en la ciudad de Bogotá durante el año 2018.

## Conclusiones
Los accidentes de tráfico en la ciudad de Bogotá durante el año 2018 generaron una gran cantidad de victimas de diferente gravedad, siendo los adultos mayores los que aportan la mayor cantidad de victimas fatales (Mayores de 61 años), sin embargo al analizar la distribución para victimas hospitalizadas y las victimas con valoración médica, se logra identificar que los jovenes entre los 16 y 23 años son los que en la mayoría de los casos resultan heridos en este tipo de incidentes.
Ahora para el caso específico de las victimas que requirieron valoración médica, la distribución esta encabezada por los jovenes entre los 16 y 23 años, seguido muy de cerca por los de 24-30 años y los de 31-40 años. Los jovenes entre 16 y 23 años son personas en edad de recibir su primera licencia de conducción y además se encuentran cursando estudios secundarios y universitarios. Para el caso de victimas hospitalizadas tambien esta encabezado por el grupo de jovenes entre los 16 y 24 años, seguido por los de 31-40 años. En conclusión los adultos mayores (Mayores de 60 años) aportan la mayor cantidad de victimas fatales, pero los jovenes entre los 16 y 23 años son los que aportan la mayor cantidad de victimas hospitalizadas y valoradas medicamente. 
Los niños entre 0 y 15 años en general resultan involucrados como victimas en menor cantidad de casos.</br></br>Los incidentes de choque y atropellamiento aportan la mayor cantidad de victimas en todos sus niveles de gravedad, pero para el caso de victimas fatales el atropellamiento es la principal causa.
## Tecnologías usadas
* D3@5
* Javascript
## Autor
Hermes Puentes Navarro https://www.linkedin.com/in/hermes-puentes-navarro-1898b2b3/
