La función **fork** es una wrapper de una [[Syscall]] que se llama clone. Lo que hace es clonar un [[Procesos|proceso]]. 

Sabemos que este tiene un montón de registros, archivos abiertos, un pid y más información que va a clonar (no todo) a lo que se llama el proceso hijo. 

En la copia que hace, cambia algo de información, como por ejemplo el pid. 
- Va a tener un parent pid (ppid) que va a tener el pid del proceso padre. 
- El RIP de este segundo proceso va a estar apuntando al mismo lugar. En caso de haber un error, el valor de retorno es -1. 
- Cuando aparece un ret dentro de la función fork se va a ejecutar 2 veces, una dentro el proceso padre y otra del proceso hijo. 
	- Para el primero, fork retorna el child pid y en el segundo retorna cero. Es decir que el padre conoce el identificador del hijo. 
	- Si queremos cambiar el código del hijo, se utiliza execve. 
	- Para ambos procesos lo que hace Linux es dejarlos compartir la RAM física y solamente copia la memoria cuando uno quiere escribir. Esto lo hace dándole a los procesos páginas de tablas iguales, pero se asegura que sean read-only. 

Cuando un proceso trata de escribir una dirección de memoria compartida:
1. Salta un page fault.
2. Linux hace una copia de la página y actualiza la tabla de páginas.
3. El proceso continúa sin enterarse.