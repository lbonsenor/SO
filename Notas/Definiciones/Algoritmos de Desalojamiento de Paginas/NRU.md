El algoritmo NRU (not recently used) utiliza los bits R y M de las tablas de páginas, que se actualizan en cada referencia. Tenemos 4 clases posibles

- Clase 0: $\neg R\wedge\neg M$
- Clase 1: $\neg R\wedge M$
- Clase 2: $R\wedge\neg M$
- Clase 3: $R\wedge M$

El bit R es puesto a 0 periódicamente por el [[Sistema Operativo|SO]] para olvidar referencias pasadas

Lo que hace el algoritmo es buscar una página de las características de la clase 0, ya que no se referenció recientemente y tampoco está modificada. Esto último permite que no se deba bajar a memoria pues no está modificado, lo que ahorra muchos recursos porque escribir en memoria es costoso. Vemos que nos estamos basando en el principio de cercanía de referencias.