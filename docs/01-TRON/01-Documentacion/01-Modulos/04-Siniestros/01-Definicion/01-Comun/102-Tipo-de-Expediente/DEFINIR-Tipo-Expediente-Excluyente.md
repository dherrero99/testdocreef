
![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Tipo de Expedientes Excluyente {#titulo}


==EN CONSTRUCCIÓN==  

## **Objetivo**
La finalidad es definir que Tipos de Expedientes, tipos de daños, __no pueden convivir en un mismo siniestro__.
Previamente se han de definir los Tipos de Expedientes y asociarlos a los Ramos.


## **Propiedades por Ramo** 
En este apartado se detallarán todos los atributos específicos para la clave del ramo que estamos definiendo.

### **Ramo**
Este atributo indica la __[clave del Ramo][ramo]__ para el que se va a definir los Tipos de Expedientes que son Excluyentes, que no puede tener un mismo Siniestro.

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Tipo de Expediente**
Este atributo será la __clave__ por la que se identifica al __tipo daño__, al cual se le va a indicar que otros Tipos de Expedientes no se podrán abrir dentro de un mismo siniestro, si ya hay un expediente con este el Tipo abierto.


### **Tipo de Expediente Excluido**
Este atributo será la __clave del tipo daño__, que será excluido, no podrá liquidarse, si ya se ha abierto previamente un expediente con el Tipo del atributo anterior y no está terminado sin pagos.

Ejemplo:   

- Tipo de Expediente: __PPD__ Pérdida Parcial - Tipo Expediente Excluyente: __PPT__ Pérdida Total

- Tipo de Expediente: __PAR__ Parto - Tipo Expediente Excluyente: __ABO__ Aborto	

## **Vínculos**

 [Definición Tipo Expediente](../102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#titulo)

## **Preguntas frecuentes**

[Preguntas y respuestas relativas al concepto de negocio]


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 


