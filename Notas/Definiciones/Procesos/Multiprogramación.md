Se denomina **multiprogramación** a una técnica por la que dos o más procesos pueden alojarse en la memoria principal y ser ejecutados concurrentemente por el procesador o CPU. 

Con la multiprogramación, la ejecución de los procesos (o hilos) se va solapando en el tiempo a tal velocidad, que causa la impresión de realizarse en paralelo (simultáneamente). 

Tener el CPU al 100% significa que en cualquier instante de tiempo, si hacemos un snapshot hay un proceso corriendo.

Un proceso pasa una proporción p del tiempo esperando por I/O (bloqueado). Con n procesos en memoria en memoria al mismo tiempo, la probabilidad de que los $n$ estén esperando (CPU libre) es $p^n$. Entonces, podemos decir que la utilización del CPU se puede expresar como $1-p^n$.