Sabemos que tenemos archivos almacenados en disco. Una manera sencilla de almacenar los archivos con el file system es asignar bloques continuos. Por ejemplo:
- Con bloques de 1KB y un archivo de 50KB, usamos 50 bloques.
- Con bloques de 2KB y el mismo archivo, usamos 25 bloques y tenemos una pequeña fragmentación interna.

Este sistema tiene dos ventajas, que son la facilidad de implementarlo (solo inicio y longitud) y un excelente rendimiento de disco (secuencial y random), pues es sencillo acceder a la información calculando con los datos guardados de inicio y longitud. 

Las desventajas son la fragmentación externa (pues cuando se liberan los bloques pueden no quedar contiguos) y que se debería conocer el tamaño a priori, pero los archivos no mantienen un tamaño constante.

![[Pasted image 20251210035416.png]]