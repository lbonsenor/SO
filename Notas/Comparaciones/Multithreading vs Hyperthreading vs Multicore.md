**Multicore:** 
- Un procesador que tiene muchos núcleos (1 chip, N CPUs)
- Hardware
- Comparten recursos
- Ejecución paralela real

**Multithreading:**
- En multicore, trabajan en paralelo, en single core, trabajan divididos
- Memoria compartida
- Software
- No garantiza ejecución simultanea
- Concurrencia, no paralelismo

Hyperthreading:
- Hardware
- Compiten por el mismo hardware
- Comparten recursos
- "Dos cocineros tienen una hornalla"
- Más limitado, es mejor para workloads mas chicas
- Paralelismo oportunistico