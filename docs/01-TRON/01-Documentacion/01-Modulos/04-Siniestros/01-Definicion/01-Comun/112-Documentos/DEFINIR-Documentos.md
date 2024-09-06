![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }
<mark>Falta:</mark> Preguntas y Respuestas

==EN CONSTRUCCIÓN==  

# DEFINICIÓN de DOCUMENTOS {#titulo}

## **Objetivo**
La finalidad es definir todos los documentos (documentación) que puedan ser necesarios para la tramitación de los diferentes tipos de expedientes.

Tendremos propiedades que serán comunes para todos los ramos y tipos de Expedientes y otras propiedades que serán propias de cada Ramo y/o Tipo de Expediente.

- [Propiedades Generales](#propiedades-generales)
- [Propiedades por Ramo](#propiedades-de-los-documentos-por-ramo)

## **Propiedades Generales**
En este apartado se detallarán todos los atributos, propiedades comunes, es decir los atributos que no cambian por ramo.

### **Documento**
Este atributo será __la clave__ por la que se va a identificar los documentos necesarios para tramitar un expediente.  
Una clave podrá ser utilizada para uno o varios ramos.

### **Nombre del Documento**
Este atributo contendrá la __descripción de la clave__ definida para el documento.  
Este Nombre es largo para que pueda ser utilizado, para el envío de una comunicación solicitando los documentos necesarios.

Ejemplo:   
	
- Documento: __1__	
- Nombre del Documento: __Documento Nacional de Identidad__

### **Nombre Corto del Documento**
Este atributo contendrá la __descripción de la clave__ corta, definida para el documento.  
Esta descripción corta será utilizada, para los programas que solicitan los documentos.

Ejemplo:  

- Documento: __1__	 
- Nombre del Documento: __Documento Nacional de Identidad__ 
- Nombre corto: __D.N.I.__

### **Identificador del Documento es Obligatorio**
Este atributo contendrá si la __identificación del documento__ cuando se reciba __es obligatorio introducirlo o No__.Ejemplo si solicitamos un documento de identificación de la persona, el número de dicho documento, es obligatorio o no registrarlo. Otro ejemplo sería si se registra que se ha recibido una factura si es obligatorio o no, introducir el número de factura.

### **Lógica que determina si el Identificador es obligatorio**
Este atributo contendrá una lógica de Negocio, para los casos en el que la obligatoriedad de registrar el identificador del documento sea obligatorio o no, dependiendo de otros parámetros, por ejemplo dependiendo de si la persona relacionada con el expediente es del país o extranjero ...

### **Lógica que valida el Identificador del Documento**
Este atributo contendrá una lógica de Negocio, para validar el identificador del documento, si este tiene una fórmula o un formato preestablecido.

### **Inhabilitado**
Este atributo indica si el Documento que está definido, está habilitado para poder asociarlo a los diferentes Ramos y/o Tipos de Expediente.

Ejemplo:  

 | Documento|Nombre| Nombre Corto|Identificador Obligatorio| Valida Identificador|Inhabilitado
  |---|---|---|---|--|---|
  |**1** |Documento Nacional de Identidad| D.N.I.|S|S|N|
  |**2** |Carnet de Conducir| Carnet de Conducir |S|N|N|
  |**3** |Foto del Accidente| Fotos |N|N|N|

## **Propiedades de los Documentos por Ramo y Tipo de Expediente**
Como se ha indicado anteriormente, los documentos están definidos a nivel de compañía, y posteriormente se asociarán a los ramos que los vayan a solicitar.
 En este apartado se detallará todos los atributos necesarios para definir el comportamiento del documento dentro de un Ramo.   

### **Ramo**
Este atributo indica la __[clave del Ramo][ramo]__ al que se va a asociar los documentos definidos previamente a nivel de compañía.  

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Tipo de Expediente**
Este atributo indica la __[clave del Tipo de Expediente][tipoexpediente]__ al que se va a asociar los documentos definidos previamente a nivel de compañía. 

[tipoexpediente]: <./DEFINIR-Tipo-Expediente.md#titulo>

### **Lógica que determina si el Identificador es obligatorio**
Este atributo contendrá una lógica de Negocio, para los casos en el que la obligatoriedad de registrar el identificador del documento sea obligatorio o no, dependiendo de otros parámetros, por ejemplo dependiendo de si la persona relacionada con el expediente es del país o extranjero ..

### **Lógica que valida Identificador del Documento**
Este atributo contendrá una lógica de Negocio, para validar el identificador del documento, si hay una fórmula o formato preestablecido

### **Inhabilitado**
  Este atributo indica si el Documento que está definido, está habilitado o deshabilitado para solicitarlo en un expediente, cuyo ramo y tipo de expediente sea el que se está definiendo.

Ejemplo:  

Aquí se está definiendo los documentos que se podrán solicitar, cuando se abra en expediente de Tipo Daños Propios Materiales, del Ramo 3 Automóviles.

| Ramo|Tipo Expediente|Documento|Identificador Obligatorio| Valida Identificador|Inhabilitado
  |---|---|---|---|--|---|
  |**300** (Autos)|**DPM** (Daños Propios Materiales)| **1** (Documento Nacional de Identidad)|S|S|N|
  |**300** (Autos) |**DPM** (Daños Propios Materiales)|**2** (Carnet de Conducir) |S|N|N|
  |**300** (Autos) |**DPM** (Daños Propios Materiales)|**3** (Atestado Policial) |S|N|N|

## **Vínculos**



## **Preguntas frecuentes**

- ¿Cuándo se soliciten los documentos, se guardará la fecha de cuando se solicitó dicho documento?  
  Si, quedará guardada tanto la fecha de cuando se solicita, como la fecha de cuando se recibió en la compañía.


- ¿Se van a poder solicitar más de un documento por Expediente?  
  Si, cuando se soliciten los documentos para un expediente, se buscarán todos los documentos que estén definidos para el Ramo y el Tipo de Daño que tenga el expediente.



[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

