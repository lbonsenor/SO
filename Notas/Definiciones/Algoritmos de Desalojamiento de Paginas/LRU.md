El algoritmo LRU (least recently used) parte de la observación de que las páginas muy usadas recientemente suelen seguir siendo muy usadas y las escasamente usadas recientemente suelen seguir sin ser muy usadas. 

Lo que busca es desalojar la página que no ha sido usada en el mayor tiempo. Hay dos enfoques para este algoritmo:
- Tener una lista de páginas ordenada por tiempo de acceso y desalojar a la más antigua. Requiere únicamente de software.

- Tener un registro especial que cuente instrucciones y equipar a cada entrada de la tabla con espacio para este registro. Cuando se referencia una página se actualiza su contador. Luego, se desaloja la que tenga el contador más chico. Requiere de hardware para funcionar.