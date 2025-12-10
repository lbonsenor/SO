[[Definiciones/Scheduling/Algoritmos/Round-Robin]] asume que todos los procesos son igualmente importantes. 

El algoritmo **Priority Scheduling** asigna prioridades a los procesos, y aquellos que tienen la mayor son elegidos primero. 

Es preemptive. La prioridad debe ser ajustada periódicamente para evitar la inanición (proceso se muere de hambre). 

Esto se puede hacer estáticamente o dinámicamente dependiendo del usuario o dependiendo del comportamiento del proceso. 

Para un proceso I/O-bound puede ser $\frac1f$ donde $f$ es la proporción del último quantum usado. Por ejemplo, si un proceso usa el 50% del quantum, tendrá una prioridad de $1/0.5 = 2$. Si usó un 25%, tiene una prioridad de $1/0.25 = 4$. Notemos que cuanto menos quantum use, más prioridad tiene.