El algoritmo **Second Chance** es como un [[Definiciones/Algoritmos de Desalojamiento de Paginas/FIFO|FIFO]] modificado. Lo que hace es un FIFO donde se mira el bit R. 

Si se encuentra prendido, se le da una segunda chance y se vuelve a cargar al final de la lista reseteando el bit, como si hubiera sido levantada recientemente. 

Si el bit es cero, se desaloja. Si todas las páginas se encuentran referenciadas, el algoritmo se convierte en FIFO ya que se desaloja la primera por la que se preguntó.