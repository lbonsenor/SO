Comando `ldd`: Indica las librerias requeridas por un archivo
- Ej: `ldd /bin/ls`

Comando `objdump`: Genera info acerca de un archivo objeto
- Los argumentos del comando retornan distinto tipo de información
    - `-f`: Muestra los file headers
    - `-h`: Muestra las secciones

Comando `ps`: Process status: Reporta una snapshot de los procesos actuales

Comando `pmap`: Reporta el mapa de memoria de un rpoceso
- Ej: `pmap -p [PID]`
- Memoria Anonima: Variables del data segment

Comando `strace`: Indica las syscalls que ejecuta el programa
- Ej: `strace -e trace=openat /bin/ls`
    - Busca ver si se corre especificamente la syscall `openat()`
- `openat()`: `open()` y `lsync()` en una sola operación 
- `fstat()` o `lstat()`: Puedo leer la metadata de un archivo
- `getdents64()`: Get directory entries, es como un `read()` pero de directorios

Comando `ltrace`: Indica todas las llamadas a funciones que ejecuta el programa

Comando `time`: Indica el tiempo que tarda en terminar un proceso
- Ej: `sudo time strace find /usr/`

Comando `bpftrace -l`: Ve todos los lugares donde puedo realizar Instrumentacion dinámica
- `tracepoint`: Puntos de instrumentacion claves
    - Ej: `sudo bpftrace tracepoint:syscalls:*` Podemos ver args y returns en las syscals
    - Ej: `bpftrace -lv tracepoint:syscalls:sys_enter_openat` Nos permite saber cual programa consume mas ciclos

Instrumentacion dinámica
- Puedo analizar/ver cuando corre un evento y correr código en ese momento
- Cuando no esté corriendo no tenga penalidad y cuando lo haga sea la mínima posible

Sistema de archivos: Todo es un archivo
- Limitaciones
    1. No puedo tener links entre dispositivos distintos
    2. No puedo crear links a directorios
- Links Simbolicos `simlink`
    - A diferencia del hard link que apunta directamenente al d:irectorio este es un tipo de archivo especial
