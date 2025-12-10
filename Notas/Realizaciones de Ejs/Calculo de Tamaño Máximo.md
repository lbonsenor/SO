Sea $n$ la cantidad de bytes que ocupa un bloque
Sea $m$ la cantidad de bytes que ocupa una dirección de disco

En caso de $k$ entradas directas: $k\cdot n$
En caso de $k$ entradas simples indirectas: $\frac{k\cdot n}{m}\cdot n$
En caso de $k$ entradas dobles indirectas: $(\frac{k\cdot n}{m})^2\cdot n$
En caso de $k$ entradas triples indirectas: $(\frac{k\cdot n}{m})^3\cdot n$