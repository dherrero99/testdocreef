![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }


==EN CONSTRUCCIÓN== 

# Definición Coberturas por Tipo de Expediente {#titulo} 

## **Objetivo**
Una vez que se han asociado los Tipos de Expediente al Ramo y se le ha definido sus características, lo siguiente es asociarle al Tipo de Daño las Coberturas y Conceptos de Reserva.
La finalidad es definir para cada tipo de Expediente (tipo de daño), las coberturas del ramo y los conceptos de reserva a los que puede afectar en caso de siniestro.  

Ejemplo  Autos:

- 
  Ramo|Tipo Expediente|Cobertura|Concepto Reserva|  
  |---|---|---|---|
  |**300** Autos |**DPM** Daños Propios Materiales| **3001**Daños Propios|**1** Indemnización|
  |**300** Autos |**DPM** Daños Propios Materiales| **3001**Daños Propios|**2** Honorarios|
  |**300** Autos |**DPM** Daños Propios Materiales| **3001**Daños Propios|**3** Gastos|

Ejemplo Vida:  

-  
  |Ramo|Tipo Expediente|Cobertura|Concepto Reserva|  
  |---|---|---|---|
  |**150** Unit Linked |**MUE** Muerte| **1500** Fallecimiento|**1** Indemnización|
  |**150** Unit Linked |**MUE** Muerte|  **1500** Fallecimiento|**3** Gastos|
   |**150** Unit Linked |**MUE** Muerte|  **1501** Inversión|**92** Capital Unidades de Participación|
  |**150** Unit Linked |**MUE** Muerte|  **1501** Inversión |**3** Gastos|
 
### **Ramo**
Este atributo indica la [clave del Ramo][ramo] al que se le va asociar a los Tipos de Expedientes, las Coberturas y Conceptos de Reserva.  

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Tipo de Expediente**
Este atributo será la [clave del Tipo de Expediente][tipoexpediente] al que se le va asociar una o varias Coberturas y Conceptos de Reserva.  
Los tipo de Expedientes tienen que estar asociados al Ramo previamente. 

[tipoexpediente]: <../102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#titulo>

### **Cobertura**
Este atributo contendrá la [clave de la Cobertura][cobertura] al que puede afectar el Tipo de Expediente que estamos definiendo.  
Un tipo de Expediente podrá afectar a una o varias coberturas del Ramo.  
Esta cobertura tiene que estar asociada previamente al Ramo.

[Cobertura]: <NoLink>

### **Concepto de reserva**
Este atributo será [la clave][conceptoreserva] por la que se va a identificar los distintos conceptos por los que se puede a reservar en el Tipo Expediente Cobertura que estamos definiendo.

[conceptoReserva]:<../103-Concepto-de-Reserva/DEFINIR-Concepto-Reserva.md#titulo>

## **Vínculos**

## **Preguntas frecuentes**
- ¿Hay que provisionar, dar valoración, a todas las coberturas y conceptos de reservas asociados al tipo de Expediente?

   No, cuando se abra el expediente se reservará únicamente a las coberturas concepto de reserva que se vean afectadas en ese expediente.  
   Por ejemplo si no hay profesionales externos, no habría que valorar los conceptos de reserva de tipo **Honorarios** (H), ni **Gastos** (G)

 - ¿Se puede asociar más de una cobertura a un Tipo de Expediente?  
    Si, el sistema permite asociar una o n coberturas por tipo de Expediente. 
    
    Por Ejemplo un expediente de Responsabilidad Civil, si el producto tuviera Responsabilidad Civil y Responsabilidad Civil Complementaria, el tipo de expediente se asociaría a las dos coberturas.
    
  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

