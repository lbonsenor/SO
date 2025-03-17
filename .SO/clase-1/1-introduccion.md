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

> [!IMPORTANT]
>
> ## Tipos de Sistemas Operativos
>
> - `Mainframe`: Mucho almacenamiento y memoria. Orientado a muchos procesos. Soporta trabajos por lotes, transacciones y timesharing. OS/390, tendencia a UNIX.
> - `Server`: Computadoras personales o incluso mainframes. Impresoras, archivos o webs. Solaris, FreeBSD, Linux y Windows Server.
> - `Multiproceso`: (Necesaria la separación)
> - `Personal Computer`: Proveer soporte a un único usuario. Linux, FreeBSD, Windows y Apple’s OS X.
> - `HandHeld Computer`: Tablets y smartphones. Android y iOS
> - `Embedded`: Electrodomésticos y teléfonos antiguos. ROM, no permite la instalación de aplicaciones. Embedded Linux, QNX y VxWorks.
> - Sensor-node: Redes de nodos. Poseen CPU RAM y ROM. Sensan diferentes condiciones. Conexión
inalámbrica. TinyOS
> - `Real Time`: Necesitamos que una acción ocurra en un momento específico. hard vs soft. Industria,
aviónica, milicia y multimedia. eCos y FreeRTOS
> - `Smart Card`: Pagos electrónicos. Del tamaño de una tarjeta de crédito. Restricciones de potencia y
memoria muy altas. Obtienen energía por inducción o al conectarse a un lector.
