![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN== 
# DEFINICIÓN de Recobros por Tipo de Expediente {#titulo}

<mark>Falta:</mark> Preguntas y respuestas, Link a documentos sin hacer, Revisar las lógicas
==EN CONSTRUCCIÓN==  

## __Objetivo__
La finalidad es definir que todos los __posibles Recobros__ que se le puede asociar a los distintos Tipos de Expedientes (No Recobros). Para poder abrir un Expediente de Recobro tiene que haber uno de No Recobro abierto, para poder asociarlo.
Antes han de estar definidos los Tipos de Expedientes y estos deben estar asociados a los Ramos.

## Propiedades por Ramo
En este apartado se detallarán todos los __atributos específicos por ramo__.

### **Ramo**
Este atributo indica __[la clave del Ramo][ramo]__ para el que se va a definir todos los posibles Tipos de Recobros que pueden tener los diferentes Tipos de Expedientes.

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Tipo de Expediente**
Este atributo será la __clave__ por la que se identifica al __[tipo daño][tipoexpediente]__, al cual se le van a asociar los distintos tipos de Expediente de Recobro que se le van a poder asociar. Este Tipo de Expediente tienen que haber sido definido como NO Recobro.

[tipoexpediente]: <../102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#titulo>

### **Tipo de Expediente Recobro**
Este atributo será la __clave__del tipo daño, que sea un __[Recobro][recobro]__, es decir que el Tipo de Expediente tiene que haber sido definido como de RECOBRO.

[recobro]: <../102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#propiedades-generales-tipos-de-expedientes-recobros>

Ejemplo: 

Tipo Expediente: __PPT Pérdida Total__

- Tipo Expediente Recobro: __SAL__ Salvamento
- Tipo Expediente Recobro: __RAA__ Recuperación Asegurado
- Tipo Expediente Recobro: __RAT__ Recuperación Tercero

En este caso al Tipo de Expediente de Pérdida Total, se le está asociando los tres posibles tipos de Expedientes de Recobro que se le van a poder abrir y asociar.  
El Tipo de Expediente de Recobro de Salvamento, para poder vender los restos del vehículo, el Tipo de Expediente de Recobro Ante del Asegurado, para poder cobrar la franquicia o deducible, y si el contrario ha tenido la culpa del siniestro, un Recobro de Recuperación del Tercero.

### **Apertura Automática** {#aperturaautomatica}

Este atributo indica si el __Tipo de Expediente de Recobro__, cuando se asocie al Tipo de Expediente que se está definiendo, __se abrirá automáticamente__.  
Cuando se apertura automáticamente, si el parámetro a nivel de compañía indica que la valoración del Expediente de Recobro es la del Expediente Principal, se tomará ese importe, si no es así, se abrirá por la reserva inicial definida para el Ramo, causa, consecuencia, Tipo de Expediente, concepto de reserva, cobertura.

### **Lógica que determina Apertura Automática**
Este atributo contendrá una lógica de Negocio, cuando no siempre se abre el Recobro o no se abre automáticamente, sino que va a depender de otros factores que no son el tipo de expediente que se está definiendo. Se tendrá que definir la lógica de Negocio que determine si se abre o no automáticamente el Recobro.

 
## Preguntas frecuentes

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
