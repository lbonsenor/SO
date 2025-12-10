En los sistemas interactivos se tiene el algoritmo **fair-share scheduling** donde se tienen dos usuarios donde uno ejecuta una cantidad de procesos y el otro usuario otra cantidad, y se le asigna una fracción del tiempo a cada uno. Si tenemos:

**Usuario 1**: procesos A B C D
**Usuario 2**: Proceso E.

Si le asignamos el 50% del CPU a cada usuario tenemos: 
A E B E C E D E A E B E C E D E ...

Si le asignamos el doble de CPU al usuario 1 que al usuario 2:

AB E CD E AB E CD E ...