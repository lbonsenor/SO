**Al usar cache, la memoria principal se divide en cache lines de 32 o 64 bytes generalmente. Siempre se almacena una cache line completa. ¿Qué ventajas hay respecto a almacenar de a 1 byte?**

Como programamos secuencialmente, lo más probable es que la siguiente instrucción
a ejecutar se encuentre en la dirección de memoria adyacente a la actual, por lo que la mayor
ventaja de traer la línea entera es hacer más eficiente la búsqueda de las instrucciones en 
memoria.