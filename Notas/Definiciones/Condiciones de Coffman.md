Las **condiciones de Coffman** son una serie de condiciones necesarias planteadas por Coffman para que un estado sea un deadlock. Si una de ellas no se cumple, ya no se está hablando de dicho estado
## Exclusión mutua
Cada recurso está actualmente asignado a exactamente un proceso o está disponible. Si un recurso pudiera asignarse a múltiples procesos, no existiría deadlock nunca. Cuando tenemos un semáforo con valor 5 y lo toman 5 procesos, cada uno es un recurso, no es que está disponible para múltiples procesos.

## Hold-and-wait
Los procesos que actualmente tienen los recursos asignados previamente pueden solicitar nuevos recursos. En el ejemplo anterior, sería el segundo down que es el que produce el deadlock.

## No-Preemption
Un recurso previamente cedido no puede ser quitado forzosamente al proceso, sino que este lo debe liberar explícitamente.

## Circular Wait
Debe haber una lista circular de dos o más procesos, cada uno esperando por un recurso mantenido por el siguiente miembro de la cadena. En realidad, se puede dar también con un único proceso que se espere a sí mismo.