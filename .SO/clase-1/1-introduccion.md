# Introducción

> [!NOTE]
>
> ## Sistema Operativo (SO)
>
> Un programa que gestiona los recursos *(hardware)* de una computadora y provee un conjunto **abstracto** y **limpio** de los mismos. Garantiza que se distribuyan de manera *"igualitaria"* entre los procesos.
>
> > **Ejemplos de recursos:** Memoria, Periféricos, Tiempo de la CPU

> [!NOTE]
>
> ## Proceso
>
> Un programa en ejecución **dentro** del contexto de un SO
> > Un proceso es el **cliente** de un sistema operativo

La `shell` es un programa común y corriente, es un proceso de usuario. Tiene una característica particular, ya que nos permite ejecutar programas arbitrarios.

> [!TIP]
>
> ## Modo `Kernel` vs Modo `User`
>
> Hay **dos** bits en el selector de segmento de código que determinan el nivel de privilegio
>
> - En modo `kernel` tengo comunicación directa con el **hardware**
> - En modo `user` solo puedo hablar con el **hardware** mediante `syscalls`
>
> El **hardware** esta diseñado para funcionar de un modo o del otro

`Multiplexación`: La división de los recursos entre **tiempo** y/o **espacio**
