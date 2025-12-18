# ¿En qué comunas se concentran más puntos para cargar tu Tarjeta Bip?

Me pareció interesante analizar cómo algunas comunas concentran una mayor cantidad de puntos de carga para el uso del transporte público, mientras que otras presentan una menor disponibilidad del servicio.

---

## Fuentes de datos
Las fuentes utilizadas fueron obtenidas desde la base pública del Gobierno de Chile. A continuación, adjunto los enlaces:

1. https://datos.gob.cl/dataset/lugares-de-carga-de-tarjeta-bip-_puntos-bip  
2. https://datos.gob.cl/dataset/lugares-de-carga-de-tarjeta-bip-_centros-bip-estandar-normal  
3. https://datos.gob.cl/dataset/lugares-de-carga-de-tarjeta-bip-_centros-bip-alto-estandar  

---

## Proceso de limpieza de datos
El proceso de limpieza fue el siguiente:

1. Cargar los DataFrames.
2. Analizar la información disponible. Utilicé la función `head()` para revisar las primeras filas y detectar posibles problemas en los datos.
3. Guardar los servicios, ya que me percaté de que estaban registrados en celdas fuera de la tabla. Posteriormente, los incluí como una descripción dentro de cada DataFrame.
4. Analizar las columnas entre los distintos DataFrames y eliminar una columna que no podía ser incluida, ya que no era posible asignar un valor coherente en los otros archivos. Finalmente, anexé los DataFrames.
5. Por último, agregué dos columnas necesarias para el panel geográfico: `país` y la concatenación de `latitud` y `longitud`, para luego exportar el archivo final.

---

## Decisiones de diseño del panel
Utilicé un enfoque de diseño que va **de lo macro a lo micro**, ya que considero que facilita la lectura y la toma de decisiones:

- En la **primera fila** incorporé métricas o KPIs, de modo que lo primero que visualice el cliente sea el estado general del desempeño.
- En la **segunda fila** agregué dos gráficos principales: un gráfico de barras con el *Top 10* de las comunas con mayor y menor cantidad de puntos de carga, permitiendo identificar rápidamente dónde se concentra el problema.
- En la **tercera fila** presenté un desglose de los puntos donde se concentran los datos. Aproveché la información de latitud y longitud para crear un gráfico geográfico y añadí una tabla de detalle que puede expandirse mediante el botón “+”. Este recurso permite que el cliente tenga toda la información necesaria para apoyar la toma de decisiones.

En general, esta es mi forma de trabajar: ir de lo general al detalle. En algunos proyectos agrego tablas más detalladas para que el cliente pueda descargar la información. En este caso, la dirección resultó útil para ese propósito. Además, incluí una tabla con el detalle de los servicios, la cual puede utilizarse como un **glosario de métricas o KPIs**. En otras ocasiones, este glosario se presenta mediante tarjetas de texto, dependiendo del contexto del proyecto.
