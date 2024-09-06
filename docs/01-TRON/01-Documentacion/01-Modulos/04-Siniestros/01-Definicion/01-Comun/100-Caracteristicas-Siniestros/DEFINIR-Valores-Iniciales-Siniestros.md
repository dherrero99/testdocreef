![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

<mark>Falta:</mark>Revisión de enlaces
==EN CONSTRUCCIÓN== 
# DEFINICIÓN de VALORES INICIALES SINIESTROS {#titulo}

## **Objetivo**
La finalidad es definir los valores iniciales de ciertos atributos, para cargarlos en las operaciones a Nivel de Siniestros, Apertura de Siniestros, Modificación, etc.


## **Propiedades de Valores Iniciales de Siniestros**

### **Ramo**
Esta propiedad o atributo, contendrá la [clave del ramo][ramo] para el que estamos definiendo valores iniciales. Si varios ramos tienen los mismos valores iniciales, se puede crear la definición para el ramo genérico (todos los ramos).

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Lógica que determina el valor inicial de la Fecha Ocurrencia**  
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial de la fecha de ocurrencia del siniestro, antes de que esta sea modificada.   
En la mayoría de las instalaciones, devuelven la fecha del día.  
Esta columna se instala cargada con una lógica de núcleo, que puede ser cambiada.

### **Lógica que determina el valor inicial de la Hora Ocurrencia** 
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial de la hora de ocurrencia del siniestro, antes de que esta sea modificada. En la mayoría de las instalaciones, no devuelven nada.   
Esta columna se instala cargada con una lógica de núcleo, que puede ser cambiada.   

### **Lógica que determina el valor inicial de la Fecha Notificación** {#valorinicialFechanotificacion}
  
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial de la fecha de notificación del siniestro a la compañía, antes de que esta sea modificada.   
Normalmente en las instalaciones, devuelven la fecha del día.  
Esta columna se instala cargada con una lógica de núcleo, que puede ser cambiada.

### **Lógica que determina el valor inicial de la Hora Notificación**  
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial de la hora de notificación del siniestro, antes de que esta sea modificada.    
Normalmente en las instalaciones devuelven la hora del día, el momento en el que se está abriendo el siniestro.  
Esta columna se instala cargada con una lógica de núcleo, que puede ser cambiada.

### **Lógica que determina el valor inicial del Número de Póliza**
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial del número de Póliza.   

Ejemplo:
El rellanar el número de Póliza automáticamente, se ha utilizado cuando se llama al programa de Apertura de Siniestros desde otra aplicación dónde el usuario ya ha introducido el número de Póliza. Para que el usuario no lo tenga que volver a introducir se rescata del número de Póliza que envía quien llama a la apertura de siniestros y se pone como valor inicial. 

### **Lógica que determina el valor inicial del Número de Riesgo**
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial del número de riesgo de la póliza a la que afecta el siniestro.
Si la póliza no es multiriesgo el sistema se encarga de recoger el riesgo. 

Ejemplo:

Hay ramos que no admiten el multiriesgo por lo que se le puede devolver un 1, pero esto ya lo realiza el sistema automáticamente

### **Lógica que determina el valor inicial de la Aplicación**
Este atributo contendrá una lógica de Negocio, que devolverá el valor inicial del número de aplicación, en el caso en que la póliza no sea Fija.

## **Vínculos**


## **Preguntas frecuentes**
Es obligatorio tener 


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

