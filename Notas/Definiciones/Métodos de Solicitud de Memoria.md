**First fit**: Comenzando desde el principio, el primer bloque suficientemente grande

**Next fit**: Comenzando desde donde quedamos, el primer bloque suficientemente grande

**Best fit**: Recorre toda la lista y elige el bloque más pequeño, pero suficientemente grande. No es muy eficiente porque requiere recorrer toda la lista, y tiene un problema con la fragmentación interna, que es porque sigue quedando libre parte del bloque.

**Worst fit**: Recorre toda la lista y elige el bloque más grande.

**Quick fit**: Para el free list, podríamos pensar en clasificar los bloques libres por tamaño frecuentemente solicitado (por ejemplo 4KB, 8KB, 12KB y 16KB). En este caso, el quick fit entrega el primer bloque de la lista correspondiente