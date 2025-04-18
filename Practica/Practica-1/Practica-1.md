1. ¿Cuáles son las 2 principales funciones de un sistema operativo?
	Syscalls
	Administracion de recursos
		Memory Management
		File System

2. Al usar cache, la memoria principal se divide en cache lines de 32 o 64 bytes generalmente. Siempre se almacena una cache line completa. ¿Qué ventajas hay respecto a almacenar de a 1 byte?
	BURST: Envia 8 veces 64 bits al bus de datos
	Para lecturas secuenciales, es probable que se lea en serie, por lo tanto conviene mas traer los 64
	`Cache miss`: Cuanto mas chico es el tamaño de la cache line, mas probable es que tengas un cache miss

3. Las instrucciones relacionadas a I/O suelen ser privilegiadas ¿Por qué?
	Se necesita un sistema de administracion de recursos, para controlar las prioridades, disponibilidad, etc.
	Seguridad

4. ¿Cómo facilita el diseño de un SO disponer de 2 modos de ejecución (kernel / user)?
	Permite reducir los privilegios a un user
	A partir del Kernel se pueden administrar los procesos, manejo de datos y de hardware, en el User se pueden crear los procesos con la seguridad de que no haya problemas de seguridad y permisos.

5. ¿Cuáles de las siguientes instrucciones debería estar permitida solo en kernel mode?
	a. Deshabilitar interrupciones
	b. Leer la hora
	c. Setear la hora
	d. Cambiar el mapeo de memoria
	`f.` Todas son correctas

6. Considere un sistema con 2 CPU y 2 threads por CPU (hyperthreading). Suponga que se inician 3 programas con tiempos de ejecución de 5, 10 y 20 ms respectivamente. ¿Cuánto demora la ejecución de estos programas? Los programas son 100% CPU bound, no se bloquea y no cambian de CPU.
	20ms

7. ¿Qué es una instrucción TRAP? Explique su uso en sistemas operativos
	TBA

8. Desde el punto de vista del programador, una syscall es como una simple función. ¿Es relevante para el programador conocer si una función resulta en una syscall?
	Es relevante por eficiencia.
