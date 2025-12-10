Una **syscall** es un llamado a función, pero al realizarlo cambiamos el modo de ejecución de user a kernel. Es decir, cambia a privilegios elevados. 

El mecanismo para realizar una system call depende de la arquitectura y debe expresarse en assembler. 

Se provee una librería para poder realizarlas desde un lenguaje de alto nivel. Es importante destacar que las syscalls son costosas de invocar, entonces nos va a importar como desarrolladores de usuario si una función las utiliza o no