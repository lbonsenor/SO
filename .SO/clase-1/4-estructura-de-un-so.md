# Estructura de un Sistema Operativo

> [!NOTE]
>
> ## Sistemas Monolíticos
>
> Todo sistema operativo se compila como un único binario y toda función tiene visibilidad del resto de las funciones
>
> Un error en cualquier función hace fallar el sistema operativo entero
>
> > **Ejemplos**: Linux, Windows 95/98, TPE de Arquitectura de Computadoras

> [!NOTE]
>
> ## Microkernels
>
> Tiene como objetivo tener la menor cantidad de código en el Kernel posible para que un error no haga fallar el sistema operativo completo
>
> Todo lo demás esta en `user-mode`
>
> > **Ejemplos**: Integrity, PikeOS, MINIX

> [!TIP]
>
> ## Mecanismo vs Política
>
> Separa responsabilidades, es una estrategia que permite reducir el tamaño del kernel

> [!NOTE]
>
> ## Virtual Machines
>
> Funciona para sandboxing, 
>
> **OBS:** No es lo mismo un container que una VM
>
> > **Ejemplos**: QEMU, VirtualBox