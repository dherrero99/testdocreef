![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Planes de Tramitación {#titulo}


==EN CONSTRUCCIÓN==  
 
## __Objetivo__
La finalidad es definir los códigos de los planes de tramitación que va a tener la compañía, para poder tramitar los expedientes.

El plan de tramitación es una guía para el tramitador, una herramienta para organizar el trabajo Esta herramienta permite mejorar y especializar la tramitación de los expedientes según su naturaleza (daños materiales, daños personales, recobros…..). 

Desde el plan se puede realizar todas las operaciones necesarias para tramitar un expediente:

- Conexión con herramientas externas a TRON.
- Conexión con todos los módulos de TRON.
- Aviso de plazos formales.
- Posibilidad de generar, enviar y hacer seguimiento de cartas.
- Posibilidad de anotaciones Libres .

Esto códigos se están definiendo a nivel de compañía. Posteriormente, se tendrán que asociar a cada [tipo de expediente][tipoexpediente] por Ramo.

[tipoexpediente]:<../../../../../../../01-TRON/01-Documentacion/01-Modulos/04-Siniestros/01-Definicion/01-Comun/102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#plantramitacion>
####  

![Imagen DEFINIR-PLANES](./00-Imagen/DEFINIR-Planes-tramitacion.png){ width="596" height="159" style="display: block; margin: 0 auto" }
####   

## Propiedades  

### **Clave del Plan de Tramitación**
Este atributo será __la clave__ por la que se va a identificar los distintos planes de tramitación, que posteriormente será asociado a uno o varios tipos de expedientes.

### **Nombre del Plan de tramitación**
Este atributo será la __descripción de la clave__ definida para el plan de tramitación. Puede contener números y/o letras. 

Ejemplo:  

* Código de Plan Tramitación: __1__   Nombre del Código de Plan Tramitación: __Plan Daños Materiales Autos__  

* Código de Plan Tramitación: __2__   Nombre del Código de Plan Tramitación: __Plan Daños de Lesiones__   

* Código de Plan Tramitación: __3__   Nombre del Código de Plan Tramitación: __Plan de Salvamentos__  

### **Nombre corto del Plan Tramitación**
En este atributo será un nombre corto del plan de tramitación para ser utilizado en aquellas pantallas, listado...etc, donde no quepa la descripción del Plan


Ejemplo: 

- Código de Plan Tramitación:		__1__  
- Nombre Código Plan Tramitación:	__Plan Daños Materiales Autos__  
- Nombre Corto del Código de Plan Tramitación:	__DANMATAUT__  


### **Inhabilitado**
Este atributo indica si el Código de Plan Tramitación que está definido, está habilitado o no, para poder asociarlo a un tipo de expediente.  

## Vínculos

## Preguntas frecuentes

- ¿Un Código de Plan pueden ser asociado a tipos de expedientes de distinto sector y/o ramo?  

    Si, los planes de tramitación pueden ser asignado a tipos de expedientes de diferentes ramos, siempre y cuando la tramitación sea la misma. 

    Por ejemplo, si se define un plan de tramitación para poder gestionar expedientes de lesionados, podría asignarse a cualquier tipo de expediente que tramite lesiones, sea del Ramo que sea.

   




