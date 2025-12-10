En los interactive systems existe un algoritmo preemptive llamado **Round-Robin**. 

Se tiene una cola circular de procesos y se va atendiendo de a uno.  Si un proceso termina o se le vence el quantum, se pasa al siguiente.

Si al finalizar sigue ready, se le quita el CPU de todos modos. 

Si el context switch es de 1ms y los quantum son de 4ms, el costo es del 20% de desperdicio. En cambio si el quantum es de 100ms, el costo es del 1% de desperdicio y un aprovechamiento del 99%.  Con esto podemos concluir que un quantum razonable es de entre 20 y 50ms.