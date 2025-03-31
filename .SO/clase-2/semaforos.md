# Fork, Shared Memory y Semaforos

> [!NOTE]
>
> ## `fork`
>
> `pid` se usa como una variable tipo `pid_t` que indica el `process_id`, se usa de la siguiente forma
>
> `pid_t pid = fork()`, el cual se le asigna el process_id de manera tal que
>
> - `pid = -1`: Error
> - `pid = 0`: Estoy dentro del hijo
> - `pid = n`: Soy el padre y `n` es el PID del hijo

> [!NOTE]
>
> ## `shm`
>
> Permite que los procesos comuniquen información compartiendo una region de la memoria
>
> - `fd shm_open(const char *name, int oflag, mode_t mode)`: Crea y abre un nuevo objeto o abre uno existente
>   - Retorna un `file_descriptor` o `-1` si hubo un error
>
> ---
>
> - `ftruncate(int fd, size_t size)`: Asigna el tamaño del objeto de la memoria compartida
>   - Retorna `-1` en caso de error y setea `errno`, en caso contrario, retorna `0`
>
> ---
>
> - `void* mmap(void addr[.length], size_t length, int prot, int flags, int fd, size_t offset)`: Mapea la memoria compartida en el espacio de la dirección virtual del proceso que la llama
>   - `prot` describe el tipo de protección, ya sea `PROT_NONE, PROT_EXEC, PROT_READ o PROT_WRITE`
>   - `flags` determina si las actualizaciones al mapeo son visibles a los otros procesos, ya sea `MAP_SHARED` o `MAP_SHARED_VALIDATE`
>   - Retorna un puntero a la zona mapeada. En caso de error, retorna `MAP_FAILED`
>
> ---
>
> - `munmap`: Desmapea la memoria compartida del espacio de la dirección virtual del proceso que la llama

> [!NOTE]
>
> ## `sem`
>
> Un semáforo es un entero de tipo `sem_t` nunca puede ser menor a 0
>
> - `sem_post()`: Incrementa el valor del semáforo
> - `sem_wait()`: Decrementa el valor del semáforo (Si ya es `0`, entonces se bloquea hasta que sea mayor que `0`)
> - `sem_init(sem_t *sem, int pshared,, unsigned int value)`: Inicializa el semaforo apuntado en `sem`
>   - `pshared` Indica si el semáforo va a ser compartido entre los threads de un proceso o entre procesos
>   - Retorna `-1` en caso de error y setea `errno`, en caso contrario, retorna `0`

