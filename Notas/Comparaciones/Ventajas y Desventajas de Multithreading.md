## Ventajas
- En Sistemas [[Multicore]], muchos threads pueden correr verdaderamente en paralelo, lo cual agiliza la velocidad de un proceso
- Muchos threads permiten que partes de un programa se mantengan "responsive" sin afectar otras partes del programa
- Uso eficiente de recursos, pues estos comparten memoria, file descriptors, sockets, entre otros
- Mas ligero que multiples procesos, pues multiples threads comparten el mismo espacio de direcciones, son mas fáciles de crear y destruir y "switchean" mas rápido que procesos

## Desventajas
- Programas con multithreading son mas difíciles de diseñar, implementar, y depurar, pues agrega problemas como race conditions, deadlocks, etc. Estos tipos de errores son difíciles de reproducir y de hacer un diagnosis
- Necesidad de sincronización, ya que los procesos comparten memoria, estos tienen que se protegidos con semáforos, operaciones atómicas o mutual exclusions
- Programas con demasiados threads pueden tardar mas tiempo haciendo context switches que haciendo trabajo mas útil (thread thrashing)
