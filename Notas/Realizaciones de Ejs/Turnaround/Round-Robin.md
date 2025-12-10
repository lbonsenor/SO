Para el round robin, como se tiene una cola circular y se le va dando un poco de procesador a cada
uno, vamos a asumir un quantum de $q=2min$ para los procesos:

A: 10 mins
B: 6 mins 
C: 2 mins
D: 4 mins
E: 8 mins

- El proceso C termina en la primera "pasada", es decir a los $3q$ mins
- El proceso D termina en la segunda "pasada" y ya no se cuenta el C, es decir a los $5q+3q$ mins
- El proceso B termina en la tercer "pasada" y ya no se cuenta el D, es decir a los $5q+4q+2q$ mins
- El proceso E termina en la cuarta "pasada" y ya no se cuenta el B, es decir a los $5q+4q+3q+2q$ mins
- El proceso A termina en la quinta "pasada" y ya no se cuenta el E, es decir a los $5q+4q+3q+2q+q$ mins

$$T=(6+16+22+28+30)/5=20.4\ mins$$
