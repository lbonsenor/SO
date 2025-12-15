**¿Cuáles de las siguientes instrucciones debería estar permitida solo en kernel mode?**
	**a. Deshabilitar interrupciones**
	**b. Leer la hora**
	**c. Setear la hora**
	**d. Cambiar el mapeo de memoria**

a. Solamente permitido en kernel mode, porque hay algunas interrupciones que se encargan de responder a eventos críticos e incluso de temas de seguridad, por lo que el user no debería deshabilitarlas.

b. Leer no pone en riesgo la seguridad del sistema, por lo tanto no es necesario

c. Solamente en kernel mode, en caso contrario otros procesos que usen la hora pueden resultar comprometidos.

d. Solamente en kernel mode, en caso contrario se podría usar para ejecutar código malicioso