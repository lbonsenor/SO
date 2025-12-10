## Tipos de Interrupciones de Timer
**Preemptive**: Elige un proceso y corre hasta que se vence un plazo establecido (la interrupción del timer), incluso si está en estado ready.

**Non-Preemptive**: Elige un proceso y corre hasta que se bloquea o hasta que libera el CPU voluntariamente. Esto lo hace con una syscall que libera el CPU pero sin bloquearlo llamada yield.

## Tipos de Scheduling
**Batch**: No hay interacción con el usuario, por lo que puede ser non-preemptive o preemptive con un quantum (cuota de tiempo que se le da a un proceso) largo. Esto se hace porque los context switch no son baratos y se perdería mucho tiempo, no necesitamos que sea “responsive”.

**Interactivo**: el usuario interactúa con el sistema. Es preemptive porque es de uso general, es decir que incluye programas arbitrarios y por lo tanto no tenemos ninguna garantía de que colaboren entre sí. Si en este caso tenemos un quantum muy largo, como de un seg, puede pasar que toquemos una tecla y pase todo ese tiempo hasta que se interrumpa el proceso ejecutándose, lo que es una eternidad.

**Real time**: Se ejecutan tareas que tienen plazos que se tienen que cumplir. Por ejemplo, una tarea se tiene que ejecutar antes de los próximos 5ms. Sorpresivamente, a veces no es necesario un scheduler preemptive.