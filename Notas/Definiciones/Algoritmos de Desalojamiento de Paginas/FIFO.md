En el algoritmo **FIFO (First In-First Out)**, se registra el tiempo en el que cada página se cargó en memoria, y simplemente se desaloja la página más antigua mediante una lista linkeada. 

En un page fault, la página al principio de la lista se elimina y la nueva página se agrega al final de la lista. Si bien parece simple y fácil de implementar, no es muy eficiente.