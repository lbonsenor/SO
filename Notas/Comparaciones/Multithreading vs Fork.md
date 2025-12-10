## Ventajas de multithreading frente a fork
- Menor consumo de recursos, pues los threads comparten memoria, file descriptors, sockets, etc. Esto evita duplicación de memoria, en cambio, un fork crea un proceso completo con su propio espacio de memoria
- Comunicación rápida entre threads, pues la comunicación entre threads es simplemente acceso a memoria compartida, entre procesos, la comunicación requiere IPC
- Creación y cambio de contexto más eficientes, lo cual lo hace ideal para tareas altamente concurrentes y de poca duración
- Cuando varias tareas deben operar sobre la **misma** estructura de datos, los hilos son más naturales y eficientes que múltiples procesos.

## Ventajas de usar fork frente a multithreading
- Seguridad y aislamiento: cada proceso tiene su propio espacio de memoria, por lo tanto un error no corrompe la memoria de otro
- Evita problemas de sincronización, ya que los procesos no comparten memoria, por lo tanto no hay race conditions, deadlocks, etc.
- Si un hilo falla, se cae todo el proceso, si un proceso hijo falla, el proceso padre puede seguir funcionando