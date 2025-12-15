**¿Cómo facilita el diseño de un SO disponer de 2 modos de ejecución (kernel / user)?**

El kernel tiene una serie de privilegios que el user no tiene. La primera ventaja de esto es la seguridad y la segunda es que le permite al SO realmente administrar recursos. 

Cuando se prende la computadora, el sistema operativo es el primer programa en ejecutarse y 
se encuentra con la máquina “en cero”, es decir que es 100% configurable. 

Entonces lo primero que hace es bloquear todo para los procesos que corran después. Incluso es él mismo el que ejecuta los otros procesos.