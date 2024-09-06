![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

<mark>Falta:</mark>Revisión de enlaces, lenguaje, superíndices, detalle de atributos

==EN CONSTRUCCIÓN==  

# DEFINICIÓN de [CONCEPTO] 

## **Objetivo**
[Describir el objetivo del concepto de negocio ]
La finalidad es definir el ...

[Ejemplo que ilustre el objetivo del concepto de negocio]

[Opcionalmente colocar accesos directos a otras partes del documento]
- [Acceso directo a #](#propiedades-grupo-1)
- [Acceso directo a ##](#atributo-1-del-grupo-1)


## **Propiedades Grupo 1**
En este apartado se detallarán todos los atributos, propiedades comunes a todos los ramos, es decir los atributos que no cambian por ramo.

### **Código 1 del Grupo 1**
Este atributo será __la clave__ por la que se va a identificar las distintas consecuencias.  
Una clave podrá ser utilizada para uno o varios ramos.

### **Nombre Código del Grupo 1**
Este atributo contendrá la __descripción de la clave__ definida para la consecuencia. Puede contener números y/o letras.

Ejemplo: 
	
- Código de Consecuencia: __1__	Nombre de la Consecuencia: __Daños al vehículo Asegurado__

[](/docs/01-Definicion/01-Modulos/01-Comunes/04-Estructura%20producto/DEFINICION-Compania.md)

### **Lógica  del Grupo 1**

Este atributo contendrá una lógica de Negocio, que podrá realizar validaciones extras en función de información introducida o información propia de la instalación.

Ejemplo:

Cuando se está capturando la causa del siniestro (Tipo 1- Origen del siniestro), para el que se está definiendo, al seleccionar la causa del siniestro se puede validar que, si se ha introducido un evento catastrófico, no se puedan elegir ciertas causas.

## **Propiedades Grupo 2**
Como se ha indicado anteriormente, los tipos de expedientes pueden tener diferente comportamiento por ramo.  
En este apartado se detallará todos los atributos necesarios para definir el comportamiento del tipo de expediente dentro de un Ramo. 
### **Atributo 2 del Grupo 2**
[Describir el objetivo del atributo]

[Ejemplo que ilustre el objetivo del atributo]

[Opcionalmente colocar vínculos/enlaces a otros documentos que ayuden a entender el atributo. Por ejemplo, si el atributo hace referencia a la estructura comercial, disponer del enlace al documento que explique esta estructura]
[](/docs/01-Definicion/01-Modulos/01-Comunes/04-Estructura%20producto/DEFINICION-Compania.md)

## **Vínculos**
[Relación de otros documentos cuya lectura es recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error]

- [Definición de Cláusulas](https://mapfrecorp-my.sharepoint.com/wiki/spaces/CTRON/pages/8714739870914085337)
- [Definición de Textos Anexos](https://mapfrecorp-my.sharepoint.com/wiki/spaces/CTRON/pages/8714739871222366209)
- [Definición de Intervenciones](https://mapfrecorp-my.sharepoint.com/wiki/spaces/CTRON/pages/8714739871229050884)
- [Definición de Coberturas](https://mapfrecorp-my.sharepoint.com/wiki/spaces/CTRON/pages/8714739870912348224)

## **Preguntas frecuentes**
[Preguntas y respuestas relativas al concepto de negocio]
[Poner las preguntas como una lista. Para la Respuesta, poner dos Espacios a final de la pregunta,  dar Enter y  TAB, para que se sitúe la Respuesta debajo]

- ¿Estos son los conceptos por los que luego se realizarán los pagos?

   No, en este apartado se están definiendo los conceptos de reserva.   
   Los conceptos de pago se definirán posteriormente y se tendrán que asociar a los conceptos de Reserva.   
  
  | Concepto Reserva|\| Concepto Cobro Pago|  
  |---|---|
  |**1** Indemnización|\| **S01** Indemnización Asegurado|
  |**1** Indemnización|\| **S02** Indemnización Clínicas |
  |**1** Indemnización|\| **S03** Indemnización Talleres |

- ¿Dónde se definen los Conceptos de Pago?  
  Los conceptos de Pago se definen en la parte de tesorería. Además de definir los conceptos de Pago también se les asocia los posibles impuestos y/o retenciones.   

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

