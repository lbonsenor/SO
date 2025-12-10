Se genera un **page fault** cuando un proceso requiere una dirección que no se encuentra en la memoria (que no está mapeada y marcada como ausente)

El [[Sistema Operativo|SO]] busca un page frame libre o desaloja uno existente y trae el que contiene la dirección buscada

## Escenarios en los que ocurre un Page Fault
- Cuando un proceso quiere acceder a un dato en una pagina que no se encuentra en memoria. El S0 debe ejecutar alguno de los algoritmos de reemplazo para obtener la nueva, y actualizar en disco si se realizaron modificaciones (bit M) .

- Cuando un proceso quiere escribir en una pagina marcada como copy on write. En dicho caso, el SO debe crear una copia de la pagina entera y remappearla.

- Cuando hay una incompatibilidad en los permisos de acceso a la pagina. En este caso, se genera una interrupción (por la MMU) que le indica al SO lo ocurrido. Este transfiere el control al handler de excepciones