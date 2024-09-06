![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Concepto de Reserva {#titulo}


==EN CONSTRUCCIÓN==  
 
## __Objetivo__
La finalidad es definir el __desglose económico__ que se va a necesitar, para __aprovisionar__ a los expedientes, de __posibles pagos__.

Cuando se va a realizar la reserva (provisión), para hacer frente a los posibles pagos de un expediente, para cada cobertura afectada, nos aparecerá el desglose económico que se haya definido.

Para cada concepto de reserva, se tendrá que indicar si este será utilizado para reservar Indemnizaciones (a un taller, a un asegurado, a una clínica, a un lesionado, a un perjudicado…), para reservar posibles Honorarios de profesionales que intervengan en el expediente (abogados externos, peritos externos…) o para realizar reservas de posibles Gastos de Profesionales que intervengan en el expediente. 

Estos conceptos se están definiendo a nivel de compañía. Posteriormente, se tendrán que asociar a cada tipo de expediente, cobertura.

## Propiedades  

### **Concepto de reserva**
Este atributo será __la clave__ por la que se va a identificar los distintos conceptos por los que se puede a reservar dentro de un expediente. 

Una clave podrá ser utilizada para uno o varios tipos de expediente, cobertura.

### **Nombre del Concepto de Reserva**
Este atributo será la __descripción de la clave__ definida para el concepto de Reserva. Puede contener números y/o letras. 

Ejemplo:  

* Concepto de Reserva: __1__   Nombre del Concepto de Reserva: __Indemnización__  

* Concepto de Reserva: __2__   Nombre del Concepto de Reserva: __Honorarios Profesionales__   

* Concepto de Reserva: __3__   Nombre del Concepto de Reserva: __Gastos de Profesionales__  

* Concepto de Reserva: __4__   Nombre del Concepto de Reserva: __Reservas Matemáticas__  

### **Tipo Concepto de Reserva**
En este atributo indicará si el concepto de reserva que se está definiendo, será utilizado para reservar posibles indemnizaciones, para reservar posibles honorarios o para reservar posibles gastos.  

Los __valores__ que puede contener son: 

* __I__ Concepto de Indemnización

* __H__ Concepto de Honorarios 

* __G__ Concepto de Gastos  

Ejemplo: 

- Concepto de Reserva:		__4__  
- Nombre Concepto Reserva:	__Honorarios a Profesionales__  
- Tipo Concepto de Reserva:	__H__  


### **Inhabilitado**
Este atributo indica si el Concepto de Reserva que está definido, está habilitado o no para asociarlo a un tipo de expediente cobertura.  

## Vínculos

## Preguntas frecuentes

- ¿Estos son los conceptos por los que luego se realizarán los pagos?

    No, en este apartado se están definiendo los conceptos de reserva.   
    Los conceptos de pago se definirán posteriormente y se tendrán que asociar a los conceptos de Reserva.   
    Los conceptos de Pago llevarán asociados los posibles impuestos y/o retenciones.   
    
    | Concepto Reserva|\| Concepto Cobro Pago|  
    |---|---|
    |**1** Indemnización|\| **S01** Indemnización Asegurado|
    |**1** Indemnización|\| **S02** Indemnización Clínicas |
    |**1** Indemnización|\| **S03** Indemnización Talleres |
    |**2** Honorarios|\| **S04** Honorarios Abogados Externos |
    |**2** Honorarios|\| **S05** Honorarios Peritos Externos |
    |**3** Gastos|\| **S06** Gastos Abogados Externos|
    |**3** Gastos|\| **S07** Gastos Peritos Externos| 


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>



