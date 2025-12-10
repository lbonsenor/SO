El algoritmo **guaranteed scheduling** (sistemas interactivos) trata de dar a cada usuario del sistema una n-ésima (1/n) del tiempo del CPU. 

Si se tiene 1 usuario con n procesos, cada proceso recibirá la n-ésima parte del tiempo del CPU. 

La idea es elegir aquel proceso que haya utilizado la menor proporción de CPU, registrando el tiempo de uso de cada usuario o proceso en término de la proporción usada. Va de la mano con la idea de darle mayor prioridad a los I/O-bound.