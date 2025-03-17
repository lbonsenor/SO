# Revisión del Hardware

> [!IMPORTANT]
>
> ## Procesador
>
> El ciclo básico del CPU es obtener la siguiente instrucción de la memoria, determinar su tipo y operandos y ejecutarlas
>
> Cada procesador tiene su conjunto de instrucciones

<details>
<summary><code>Flags en 32-bit</code></summary>

![alt text](https://raw.githubusercontent.com/K0deless/k0deless.github.io/master/assets/img/introduction-re/32-bit-eflags.jpeg)

| Bit # | Mask          | Abbv.  | Name                                                                                                  | `=1`                                                                                                         | `=0`                                                                                                           | Description                                                                                         |
| ----- | ------------- | ------ | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| 0     | `0x0001`      | `CF`   | [Carry flag](https://en.wikipedia.org/wiki/Carry_flag)                                                | CY (Carry)                                                                                                   | NC (No Carry)                                                                                                  | Indica si hubo acarreo en una operación aritmética.                                                 |
| 1     | `0x0002`      | `-`    |                                                                                                       |                                                                                                              |                                                                                                                |                                                                                                     |
| 2     | `0x0004`      | `PF`   | [Parity flag](https://en.wikipedia.org/wiki/Parity_flag)                                              | PE (Parity Even)                                                                                             | PO (Parity Odd)                                                                                                | Se activa si el número de bits en 1 es par.                                                         |
| 3     | `0x0008`      | `-`    |                                                                                                       |                                                                                                              |                                                                                                                |                                                                                                     |
| 4     | `0x0010`      | `AF`   | [Auxiliary Carry flag](https://en.wikipedia.org/wiki/Half-carry_flag#The_Auxiliary_Carry_Flag_in_x86) | AC (Auxiliary Carry)                                                                                         | NA (No Auxiliary Carry)                                                                                        | Indica acarreo entre los bits 3 y 4 (usado en BCD).                                                 |
| 5     | `0x0020`      | `-`    |                                                                                                       |                                                                                                              |                                                                                                                |                                                                                                     |
| 6     | `0x0040`      | `ZF`   | [Zero flag](https://en.wikipedia.org/wiki/Zero_flag)                                                  | ZR (Zero)                                                                                                    | NZ (Not Zero)                                                                                                  | Se activa si el resultado de una operación es cero.                                                 |
| 7     | `0x0080`      | `SF`   | [Sign flag](https://en.wikipedia.org/wiki/Sign_flag)                                                  | NG (Negative)                                                                                                | PL (Positive)                                                                                                  | Indica el signo del resultado (1 si es negativo).                                                   |
| 8     | `0x0100`      | `TF`   | [Trap flag](https://en.wikipedia.org/wiki/Trap_flag "Trap flag") (single step)                        |                                                                                                              |                                                                                                                | Habilita la ejecución en modo paso a paso.                                                          |
| 9     | `0x0200`      | `IF`   | [Interrupt enable flag](https://en.wikipedia.org/wiki/IF_\(x86_flag\) "IF (x86 flag)")                | EI (Enable Interrupt)                                                                                        | DI (Disable Interrupt)                                                                                         | Habilita o deshabilita interrupciones externas.                                                     |
| 10    | `0x0400`      | `DF`   | [Direction flag](https://en.wikipedia.org/wiki/Direction_flag "Direction flag")                       | DN (Down)                                                                                                    | UP (Up)                                                                                                        | Controla la dirección de operaciones con cadenas.                                                   |
| 11    | `0x0800`      | `OF`   | [Overflow flag](https://en.wikipedia.org/wiki/Overflow_flag "Overflow flag")                          | OV (Overflow)                                                                                                | NV (Not Overflow)                                                                                              | Indica desbordamiento en operaciones con signo.                                                     |
| 12-13 | `0x3000`      | `IOPL` | [I/O privilege level](https://en.wikipedia.org/wiki/IOPL "IOPL")                                      |                                                                                                              |                                                                                                                | Controla el nivel de privilegio para operaciones de I/O. (286+ only), always all-1s on 8086 and 186 |
| 14    | `0x4000`      | `NT`   | Nested task flag                                                                                      |                                                                                                              |                                                                                                                | Indica si la tarea actual es anidada. (286+ only), always 1 on 8086 and 186                         |
| 15    | `0x8000`      | `MD`   | Mode flag                                                                                             | (NEC only)  <br>Native Mode  <br>([186](https://en.wikipedia.org/wiki/Intel_80186 "Intel 80186") compatible) | (NEC only)  <br>Emulation Mode  <br>([8080](https://en.wikipedia.org/wiki/Intel_8080 "Intel 8080") compatible) | Indica si se está en modo de depuración.                                                            |
| 16    | `0x0001 0000` | `RF`   | Resume flag                                                                                           |                                                                                                              |                                                                                                                | Permite reanudar tras una excepción de depuración.                                                  |
| 17    | `0x0002 0000` | `VM`   | [Virtual 8086 mode](https://en.wikipedia.org/wiki/Virtual_8086_mode "Virtual 8086 mode") flag         |                                                                                                              |                                                                                                                | Indica si se ejecuta en modo virtual 8086.                                                          |
| 18    | `0x0004 0000` | `AC`   | Alignment Check                                                                                       |                                                                                                              |                                                                                                                | Activa la verificación de alineación de memoria.                                                    |
| 19    | `0x0008 0000` | `VIF`  | [Virtual interrupt flag](https://en.wikipedia.org/wiki/Virtual_8086_mode#VME "Virtual 8086 mode")     |                                                                                                              |                                                                                                                | Indica el estado virtual de interrupciones.                                                         |
| 20    | `0x0010 0000` | `VIP`  | [Virtual interrupt pending](https://en.wikipedia.org/wiki/Virtual_8086_mode#VME)                      |                                                                                                              |                                                                                                                | Indica si hay interrupciones virtuales pendientes.                                                  |
| 21    | `0x0020 0000` | `ID`   | Able to use [CPUID](https://en.wikipedia.org/wiki/CPUID "CPUID") instruction                          |                                                                                                              |                                                                                                                | Permite la detección de CPUID en procesadores modernos.                                             |

</details>

> [!TIP]
>
> ## Multithreading
>
> Mantener el estado de 2 threads e intercambiar entre ellos rápidamente cuando sea necesario. No es paralelismo

> [!TIP]
>
> ## Multicore
>
> Replicar los núcleos independientes. Pueden soportar múltiples threads

> [!IMPORTANT]
>
> ## Memoria
>
> Idealmente, la memoria debe ser:
>
> - **Rápida** (más que la ejecución de una instrucción)
> - **Grande** (para albergar a todos los procesos juntos)
> - **Barata**

| Jerarquía                | Capacidad Típica | Tiempo de Acceso | Ejemplos de cache                    |
| ------------------------ | ---------------- | ---------------- | ------------------------------------ |
| Registros                | <1 KB            | 1 ns             | Cuándo guardar                       |
| Cache (SRAM)             | 4 MB             | 2 ns             | Dónde guardar                        |
| Memoria Principal (DRAM) | 1-8 GB           | 10 ns            | Qué entrada eliminar si hace falta   |
| Disco Sólido             | 500 GB           | 25 µs            | Dónde guardarlo en memoria principal |
| Disco Magnético          | 1-4 TB           | 10 ms            | Dónde guardarlo en memoria principal |

> [!IMPORTANT]
>
> ## Disco
>
> Dada una posición de los cabezales, cada cabezal puede leer un **track**, todos los **tracks** forman un **cylinder**
>
> Cada **track** esta dividido en **sectors**

<details>
<summary><code>Estructura de un Disco Mecánico</code></summary>

![alt text](https://www.computersciencejunction.in/wp-content/uploads/2022/09/disk-structure-in-os.jpg)

</details>

> [!IMPORTANT]
>
> ## Dispositivos I/O
>
> Hay **tres** formas de I/O
>
> 1. `Busy waiting`: Una consulta constante de finalización de una instrucción, suele ser bastante ineficiente
> 2. `Interrupción`
> 3. `DMA (Direct Memory Access)`: Transfiere datos entre hardwares sin la necesidad de un CPU

> [!TIP]
>
> ## Boot
>
> La **placa madre** posee un programa llamado **BIOS** *(Basic I/O System)* Flash RAM, no volátil pero actualizable por el **SO**
>
> La **BIOS** posee instrucciones para interactuar con la **pantalla, teclado, y disco**
>
> 1. Chequea cuánta memoria tenemos y si ciertos dispositivos como el teclado están instalados y responden correctamente.
> 2. Escanea buses PCIe y PCI en busca de dispositivos instalados.
> 3. Determina el dispositivo de boot.
> 4. Se carga el primer sector en memoria y se ejecuta
> 5. Este sector suele leer una tabla de particiones y se se carga un segundo sector
> 6. Se carga en memoria el SO y se ejecuta.
> 7. El SO consulta a la BIOS los dispositivos conectados