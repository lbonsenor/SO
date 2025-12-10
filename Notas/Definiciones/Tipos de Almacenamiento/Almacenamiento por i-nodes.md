Otra metodología de almacenamiento son los i-nodes, donde cada archivo del sistema contiene  su i-node que contiene atributos y la lista de bloques.  

Los i-nodes sólo tienen que estar en memoria si el archivo es abierto por algún proceso.

El esquema de i-node requiere un array en memoria cuyo tamaño sea proporcional al máximo numero de archivos que pueden ser abiertos al mismo tiempo 