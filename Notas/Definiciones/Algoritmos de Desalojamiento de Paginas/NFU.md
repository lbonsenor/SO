El algoritmo **NFU (Not Frequently Used)** se requiere un contador (software) para cada página. 

Periódicamente se suma el bit R de cada página a su contador (además del reseteo que sufre normalmente). 

Para desalojar, toma la que tenga el contador más chico, lo que significa que fue referenciada pocas veces, mientras que un contador grande significa que fue referenciada muchas veces. 

El problema que puede tener este algoritmo, es que una página que se utiliza muy intensamente por un proceso tendrá un contador muy alto, y si luego se pasa a otra parte del programa o termina, ese valor se mantiene, haciendo que sea más difícil para un proceso nuevo mantener sus páginas.