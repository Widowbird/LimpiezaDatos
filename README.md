# ¿En qué comuna se concentran más puntos para cargar tu Tarjeta Bip?
  Me parecio interesante ver como algunas comunas aglomeran tanta facilidad para utilizar el serivicio publico y otras no.
# Las fuentes utilizadas fueron obtenidas desde la base publica del gobierno de Chile, adjunto link
 1. https://datos.gob.cl/dataset/lugares-de-carga-de-tarjeta-bip-_puntos-bip
 2. https://datos.gob.cl/dataset/lugares-de-carga-de-tarjeta-bip-_centros-bip-estandar-normal
 3. https://datos.gob.cl/dataset/lugares-de-carga-de-tarjeta-bip-_centros-bip-alto-estandar
# El proceso de limpiezaq fue el siguiente
  1. Cargar los DataFrame
  2. Analizar la iformación que tenia, utilice la función Head para ver sus primeras filas y detectar problemas
  3. Guardar los servicios, ya que me percate que estaban anotados en unas celdas y no dentro de la tabla, estos luegos los incluí y agregue una descripción de cada DF
  4. Analice la scolumnas entre los DFs y elimine una columna que no podia incluir, ya que no sabria que valor agregar en los otros DFs, y termine anexando.
  5. Por último, agrega 2 columnas para mi panel geografico, pais y la concatenación de latitud y longitud, para terminar exportando el archivo.
# Las decisiones de diseño del panel
  Utilice un diseño que me gusta mucho, que es de lo macro a lo micro, donde la primera fila tengo metricas o Kpis, asi lo primero que ve el clientes es si van bien o mal;
  como segunda agrego 2 graficas de peso, una grafica de barra para mostrar el top 10 de los mejores y peores, asi el cliente puede identificar rapidamente en que lugar esta el problema;
  y para la tercera fila, un desglose de los puntos donde se concentran los datos, aproveche que teniamos latitud y longitud para hacer un grafico geografico y agregue una tabla de detalle,
  que si seleccionan el más se puede expandir, me gusta mucho usarla para que al final tengo todo lo que necesite el cliente para tomar una decisión.
  Mayormente esa es mi forma de trabajar, de macro a micro o de lo general al detalle, en algunos proyectos agrego una tabla con mas detalle para que el cliente descargue la información,
  aqui fue util la dirección por si la queria mi cliente.
  Además, agregue una tabla con el detalle de los servicio, que pueden usar como glosario de las metricas o Kpis, en este caso utilice la tabla, pero han habido ocasiones donde toca agregar
  tarjetas con texto para el glosario de metricas o Kpis.
