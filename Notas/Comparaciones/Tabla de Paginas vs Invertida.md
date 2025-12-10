En una Tabla de Paginas:
- Cada proceso tiene su propia tabla
- La tabla esta indexada por numero de pagina virtual
- Cada entrada apunta al page frame correspondiente
- En caso de que haya direcciones virtuales muy grandes, es necesario aplicar paginación multinivel
- Búsqueda directa y acceso rápido ([[Translation Lookaside Buffer]])

En una Invertida:
- Existe una sola tabla para todo el sistema
- La tabla esta indexada por numero de pagina física
- Cada entrada contiene información sobre que proceso y que pagina virtual ocupa ese marco
- Ahorra mucha memoria en sistemas con una EDV grande
- Traducción mas compleja, necesita hashing
- Se utiliza en sistemas donde la memoria es mas limitada