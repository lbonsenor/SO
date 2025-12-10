Hay una versión de [[Shortest Remaining Time Next]] para sistemas interactivos que se conoce como **Shortest Process Next**. 

Dijimos que es difícil saber cuándo un proceso va a ser corto. Podemos estimarlo en base a su comportamiento previo. La estimación es $T_0$ y su próxima ejecución es $T_1$. Se puede actualizar la estimación con la siguiente fórmula:

$aT_0 + (1-a)T_1$, donde a va entre 0 y 1.

Dependiendo de la cantidad de Ts dados, se puede calcular un estimado mas preciso
