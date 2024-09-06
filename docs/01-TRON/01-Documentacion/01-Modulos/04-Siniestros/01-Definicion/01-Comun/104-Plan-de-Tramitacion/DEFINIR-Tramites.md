![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de los Trámites {#titulo}


==EN CONSTRUCCIÓN==  
 
## __Objetivo__
La finalidad es definir los códigos de los niveles que van a tener los planes de tramitación. Los niveles son **códigos que agrupan trámites de la misma naturaleza**.  

Por Ejemplo:   
El Nivel de Peritaciones, agrupará a todos los trámites necesarios para gestionar las peritaciones, el Nivel de Juicios, agrupará todos los trámites necesarios para gestionar los juicios, etc.

Estos códigos se están definiendo a nivel de compañía. Posteriormente, los niveles se tendrán que asociar a los Planes, para indicar para cada Plan que niveles de tramitación van a poder tener. Posteriormente cada nivel se le va a asociar todos los trámites que se van a poder ejecutar dentro de ese nivel.

####  

![Imagen DEFINIR-NIVELES](./00-Imagen/DEFINIR-Niveles.png){ width="596" height="159" style="display: block; margin: 0 auto" }
####   

## Propiedades  

### **Clave de Nivel**
Este atributo será __la clave__ por la que se va a identificar los distintos Niveles de tramitación, que posteriormente serán asociados a uno o varios Planes.

### **Nombre del Nivel de tramitación**
Este atributo será la __descripción de la clave__ definida para el Nivel de tramitación. Puede contener números y/o letras. 

Ejemplo:  

* Código de Nivel Tramitación: __1__   Nombre del Código de Nivel Tramitación: __Nivel Comunicación con Asegurado__  

* Código de Nivel Tramitación: __2__   Nombre del Código de Nivel Tramitación: __Nivel de Peritaciones__   

* Código de Nivel Tramitación: __3__   Nombre del Código de Nivel Tramitación: __Nivel de Juicios__  

### **Nombre corto del Nivel Tramitación**
En este atributo será un nombre corto del Nivel de tramitación para ser utilizado en aquellas pantallas, listado...etc, donde no quepa la descripción del Nivel.


Ejemplo: 

- Código de Nivel Tramitación:		__1__  
- Nombre Código Nivel Tramitación:	__Nivel Comunicación con Asegurado__  
- Nombre Corto del Código de Nivel Tramitación:	__COMUNIASEG__  


### **Inhabilitado**
Este atributo indica si el Código de Nivel de Tramitación que está definido, está habilitado o no, para poder asociarlo a un Plan de Tramitación.  

## Vínculos

## Preguntas frecuentes

- ¿Un Código de Nivel pueden ser asociado a varios Planes de Tramitación?  

    Si, los Niveles de tramitación pueden ser asociados a varios planes ya que dependiendo del plan, ese nivel puede tener distintas características.  
    Por ejemplo, si se define un Nivel de Juicios para un plan puede ser que salga inicialmente, y para otro plan ese nivel no saldrá inicialmente pero si se necesita se puede incluir en el Plan para trabajar con sus trámites.
   




