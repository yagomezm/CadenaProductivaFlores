# Exportación de productos que hacen parte de la Cadena Productiva Flores - Período 2009 -2017

Este proyecto permite ver cómo ha sido el comportamiento en la exportación de  bulbos en estado vegetativo, musgos-líquenes y  plantas vivas en Colombia en el período 2009 a 2017, visualizando la cantidad de toneladas enviadas por año, mes y cuáles han sido los principales países destino.

Los datos utilizados fueron tomados de Datos Abiertos de Colombia:https://www.datos.gov.co/Agricultura-y-Desarrollo-Rural/Cadena-Productiva-Flores-Exportaciones/hieb-cqrb


Realizado por: Yenny A. Gómez

Curso: Visual Analytics

Licencia MIT

Objetivo del proyecto: Comparar en un período de tiempo (2009 a 2017) la tendencia que ha tenido la exportación de 3 productos que hacen parte de la cadena productiva de flores.

Tecnologías Usadas

Se utilizaron las siguientes tecnologías:
- IBM SPSS para el procesamiento y agregación de los datos
- Sublime Text 3
- HTML y CSS
- Librería D3.js Versión 5 para la representación de los idioms e interacciones del proyecto.
- GitHub para almacenar el código de la visualización y de los datos usados. 

Cómo se ejecuta

El proyecto esta almacenado en el repositorio de GitHub: https://github.com/yagomezm/CadenaProductivaFlores y para acceder a ver la página principal del proyecto se habilitó el servicio de GitHub Pages a la cual se accede desde un navegador https://bit.ly/2Cv4GJh.

Este trabajo se basa en el código de Knok16: https://github.com/knok16/d3-climate-change

Para lograr esta visualización se trabajó con el Framework de Tamara Munzner y a continuación se describen los pasos realizados:

# Abstracción de datos (What)
El dataset utilizado es de tipo Temporal,contiene 79.772 (items) y 18 atributos,para la realización del proyecto se tomaron los atributos:
- Anio(Year) : Ordenado - cuantitativo - secuencial
- Mes (Months): Ordinal - Cíclico
- PaísDestino (Countries): Categórico
- Toneladas (por mes):Ordenado - cuantitativo -secuencial
- Producto: Categórica

Se derivaron atributos como:
- Promedio de toneladas exportadas por año
- Total de toneladas exportadas por año y país.

# Abstracción de Tareas (Why)

Tarea Principal

Compare - Trends, de las exportaciones de los tres productos que hacen parte de la cadena productiva de flores. 

Tareas secundarias:

1. Derive - Features, se deriva el atributo promedio de toneladas exportadas por año, utilizada en el line chart, al igual que el atributo total toneladas exportadas por año a un país.
2. Identify - Trends, permite identificar un producto y su comportamiento en el tiempo.
3. Summarize - Features, para ver el comportamiento global de las exportaciones por producto y toneladas en un determinado año para un país destino.
4. Compare- Distribution,Compara las toneladas exportadas por año a cada país por producto versus el total de exportaciones del año y en el bar chart compara las toneladas exportadas por mes en un determinado año.

# Marcas y Canales (How)

Para la tarea principal y la tarea secundaria 2 se utiliza el idiom: multi series line chart
Marcas: líneas
Canales: 
- Posición horizontal express, para la variable años. 
- Posición Vertical express, para representar las toneladas promedio por año exportadas.
- Color hue para representar el producto.
El multi line chart permite hacer juxtapose.

Para las tareas secundarias 3 y 4, se utiliza el idiom: bar chart
Marcas: líneas
Canales:
Para el bar chart donde se muestran los meses los canales son:
- Posición vertical express, para las toneladas exportadas por mes
- Posición horizontal separate, order, para mostrar los meses.
- Longitud express, toneladas exportadas por mes y producto.

Para el barchart donde se muestran los países los canales son:
- Posición vertical express, para las toneladas exportadas por año
- Posición horizontal separate, order, para mostrar los países.
- Longitud express, toneladas exportadas por año y producto.

# Interacciones
En el multi-line chart se observa la tendencia de exportaciones por producto y toneladas promedio en el período 2009 a 2017, al elegir un año, en el bar chart de la izquierda se podrá observar como fue la distribución de toneladas exportadas por mes y en el barchart de la parte inferior se observarán los países a donde se realizaron las mayores importaciones en el año filtrado distribuídas por producto. 


# Insights

- Observando las distribuciones de exportaciones a los países se observa que la mayoría de países que importan estos follajes son de América, siendo que las flores tienen gran acogida en los países Europeos y asiáticos.
- En las distribuciones por países se puede ver como Curazao presentó un importante crecimiento en la importación de musgos y líquenes del año 2016 con 71.76 toneladas pasó a 2017 con 314.08 toneladas.
- Observando la tendencia en el multi line chart por producto podemos ver cómo a partir del año 2013 el producto de musgos y líquenes ha presentado mayor crecimiento que las plantas vivas y los bulbos en reposo vegetativo.
- En el bar chart donde se muestra la información por meses se observa que de la serie de años 2009-2017 el mes de marzo del año 2009 fue el mes donde mayores exportaciones de musgo y líquenes se hicieron (820.94) de las cuales fue Curazao el país destino con mayores importaciones 747.17 toneladas.

