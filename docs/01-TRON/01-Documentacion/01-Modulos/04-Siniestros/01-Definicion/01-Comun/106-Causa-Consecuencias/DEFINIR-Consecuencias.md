![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==  

# DEFINICIÓN de Consecuencias {#titulo} 

<mark>Falta:</mark> Enlaces con Terceros Tramitadores
## __Objetivo__

La finalidad es definir todas las consecuencias que se puedan derivar de un siniestro, es decir __todos los daños que se puedan producir a raíz de un siniestro__, tales como daños al vehículo asegurado, daños personales asegurado, muerte del asegurado, daños personales a terceros, daños materiales a terceros… etc.

Habrá que definir tanto los atributos generales de las consecuencias (utilizados por todos los ramos), como los atributos específicos para el ramo. 
Cuando se le asocie al ramo, se va asociar a cada causa de tipo 1(Origen del siniestro) todas las posibles consecuencias que se podrán derivar 

## **Propiedades Generales**
En este apartado se detallarán todos los atributos de las consecuencias comunes a todos los ramos, es decir los atributos que no cambian por ramo.

### **Código de la Consecuencia**

Este atributo será __la clave__ por la que se va a identificar las distintas consecuencias.  
Una clave podrá ser utilizada para uno o varios ramos.

### **Nombre de la Consecuencia**

Este atributo contendrá la __descripción de la clave__ definida para la consecuencia. Puede contener números y/o letras.

Ejemplo: 
	
- Código de Consecuencia: __1__	Nombre de la Consecuencia: __Daños al vehículo Asegurado__
- Código de Consecuencia: __2__    Nombre de la Consecuencia: __Daños Materiales Terceros__
- Código de Consecuencia: __3__	Nombre de la Consecuencia: __Daños Personales Terceros__

### **Pregunta asociada a la Consecuencia** {#preguntaconsecuencia}

Este atributo contendrá la __pregunta asociada a la clave definida__ para la consecuencia.  
El sistema permite que se muestre la descripción de la clave de la consecuencia o la pregunta asociada a la clave.  
Puede contener números y/o letras.

Ejemplo :

Código de Consecuencia: __1__

- Nombre de la Consecuencia: Daños al vehículo Asegurado
- Pregunta de la Consecuencia: __¿Hay daños al vehículo Asegurado?__

Código de Consecuencia: __2__

- Nombre de la Consecuencia: Daños Materiales a Terceros
- Pregunta de la Consecuencia: __¿Hay Daños Materiales a Terceros?__

### **Inhabilitada**

Este atributo indica si la consecuencia que está definida está habilitada para poder ser asociada a un ramo, o por el contrario, ya no está habilitada para poder ser utilizada en la definición de consecuencias por Ramo.

## Vínculos
Para que se muestre la descripción de la consecuencia o la pregunta, hay un atributo en la definición del tramitador que indica si para ese [tramitador][tramitador], se muestra la descripción de la consecuencia o la pregunta.

[tramitador]: <noLink>

## Preguntas frecuentes


- ¿Cuándo la causa es no tramitable se van a pedir las consecuencias?

    No, cuando la causa no es tramitable no se van a pedir las consecuencias por lo que no se podrán abrir expedientes hasta que la causa no sea modificada por una causa tramitable.
    
- ¿Se pueden utilizar las mismas consecuencias para varios ramos?

  Si, esta definición es a nivel de compañía para que puedan ser reutilizadas para varios ramos. Posteriormente a esta definición, se se tendrán que definir por Ramo, cada causa del ramo que consecuencias puede tener.


  

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
