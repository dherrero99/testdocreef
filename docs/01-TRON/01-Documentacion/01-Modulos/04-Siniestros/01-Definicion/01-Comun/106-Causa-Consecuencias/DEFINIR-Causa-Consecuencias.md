![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

<mark>Falta:</mark>Revisión de enlaces, Preguntas

==EN CONSTRUCCIÓN== 

# DEFINICIÓN de Causa origen  Consecuencia {#titulo}

## **Objetivo**

La finalidad es asociar al ramo por cada causa a qué consecuencias definidas en el ramo va a poder afectar, a qué Tipo de Expediente, Cobertura y Concepto de Reserva.  
Para cada combinación definiremos el importe inicial y el importe máximo.


- [Causas Consecuencias Por Ramo](#Causas-Consecuencias-Por-Ramo)
- [Tipo de Expediente por Causa Consecuencia](#Tipo-de-Expediente-por-Causa-Consecuencia)
- [Cobertura del Tipo de Expediente por Causa Consecuencia](#Tipo-de-Expediente-por-Causa-Consecuencia)
- [Importe Inicial por Causa Consecuencia Tipo de Expediente Cobertura]()
- [Importe Máximo por Causa Consecuencia Tipo de Expediente Cobertura]()


## **Causas Consecuencias Por Ramo**
En este apartado se detallarán todos los atributos, propiedades,  que habrá que definir por ramo para cada causa, consecuencia.

### **Ramo**
Este atributo será __[la clave del ramo][ramo]__ para la que estamos definiendo las causas consecuencias.

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Causa**
Este atributo será la clave de la [causa][causas] a la que estamos asociando las posibles consecuencias.  
Sólo se podrán asociar las causas tipo 1 (origen de siniestro), que previamente se hayan definido a nivel de compañía y asociado al ramo.  

[causas]:<./DEFINIR-Tipo-Causa.md#titulo>

### **Consecuencia**
Este atributo será __la clave de la consecuencia__ que vamos a asociar a la causa.  
Sólo se podrán asociar las [consecuencias][consecuencias] que previamente se hayan definido a nivel de compañía. 

[consecuencias]:<./DEFINIR-Consecuencias.md#titulo>

### **Secuencia**
Esta propiedad indicará el orden en el que las consecuencias aparecerán en la pantalla, en el caso de que es elija la causa a la que están asociadas.

### **Inhabilitado**
Este atributo indica si la causa consecuencia está inhabilitada  o habilitada.

Ejemplo  Autos: 

- 
  Ramo|Causa|Consecuencia|Secuencia|Inhabilitada|  
  |---|---|---|---|--|
  |**300** Autos |**3001** Despiste| **3010** Daños Propios |1| N|
  |-- |--| **3011** Lesionados Vehículo Asegurado|2| N|
  |-- |--| **3012** Daños Materiales Vehículos Contrarios|3| N|
  |-- |--| **3010** Daños Materiales Otros Daños|4| N|
  |-- |--| **3010** Lesionados |5| N|
  
Ejemplo Vida:  

-  
   Ramo|Causa|Consecuencia|Secuencia|Inhabilitada| 
  |---|---|---|---|--|
  |**150** Unit Linked |**1510** Muerte| **1500** Fallecimiento|1| N|
  | -- |--| **1501** Inversión|1| N
  

## **Tipo de Expediente por Causa Consecuencia**

### **Tipo de Expediente**
Este atributo será __la clave del tipo de Expediente__ que vamos a asociar a la causa y a la consecuencia.  
Sólo se podrán asociar los [tipos de expediente][tipoexpediente] que previamente se hayan definido a nivel de compañía y se hayan asociado posteriormente al ramo que estamos definiendo.  

[tipoexpediente]:<./DEFINIR-Tipo-Expediente.md#titulo>

### **Cobertura**
Este atributo será __la clave de la cobertura__ que vamos a asociar a la causa, a la consecuencia y al Tipo de Expediente
Sólo se podrán asociar las [coberturas][coberturastipo] que previamente hayamos definido para el tipo de expediente.

[coberturastipo]:<./DEFINIR-Coberturas-Tipo-Expediente.md#titulo>

### **Obligatorio**
Este atributo indica, si es obligatorio que el siniestro tenga un expediente de este Tipo. Si es obligatorio abrirlo y no se abre, el sistema no te dejará registrar el siniestro, al menos que el parámetro a nivel de compañía lo permita.

### **Anula Póliza**
Este atributo indicará si la apertura de este tipo de Expediente, supone la anulación de la póliza, si esta sólo tiene un riesgo, o la anulación del riesgo.
Ejemplo:

Si el expediente es de Muerte, una vez que se abra este tipo de expediente, habrá que anular la póliza si sólo tiene un riesgo o habrá que anular el riesgo si la póliza es multi-riesgo.

Si es un expediente de Pérdida Total, una vez que se abra este tipo de expediente, habrá que anular la póliza.

### **Inhabilitado**
Esta Marca indicará si esta combinación de Causa-Consecuencia-Tipo de Expediente, Cobertura está habilitado o inhabilitado y ya no se puede utilizar en la apertura de Expedientes.

### **Concepto de Reserva**
Este atributo contendrá el concepto de reserva que se puede valorar y liquidar para la Causa, Consecuencia, Tipo de Expediente y Cobertura.
El [concepto de reserva][conceptoreserva] tiene que estar previamente asociado al Tipo de Expediente, para poder incluirlo en esta definición.

[conceptoreserva]:<./DEFINIR-Coberturas-Tipo-Expediente.md#titulo>

### **Importe inicial**
Este atributo contendrá el importe por el que inicialmente se va a abrir el Tipo de Expediente, Cobertura y Concepto de Reserva a no ser que se introduzca manualmente otro importe.

### **Lógica que determina el Importe inicial**
Este atributo contendrá una lógica de Negocio que determinará el importe inicial por Tipo de Expediente, Cobertura y Concepto de Reserva, cuando este importe no sea fijo, sino que dependa de otros factores.

### **Lógica que determina el Importe Máximo** {#logica-importe-maximo}
Este atributo contendrá una lógica de Negocio que determinará el importe máximo de reserva por Tipo de Expediente, Cobertura y Concepto de Reserva.

Si no tenemos lógica de Negocio definida, se interpretará que el importe máximo es el capital de la cobertura.

### **Importe aplica en las Liquidaciones**
Este atributo indicará al sistema si la lógica de Negocio del importe máximo además de afectar a las reservas, aplica también a las liquidaciones.

## **Vínculos**

## **Preguntas frecuentes**
 - ¿Puede existir dentro de una misma causa dos consecuencias que afecten al mismo Tipo de Expediente, Cobertura, Concepto de Reserva?  
  Si puede existir, pero estas consecuencias serán excluyentes, es decir si se selecciona una, no se podrá seleccionar la otra.

- ¿Qué pasa si dos consecuencias afectan al mismo expediente, cobertura y distinto concepto de reserva, se abren dos expedientes?  
  No, se abre un sólo expediente con la misma cobertura y distinto concepto de reserva.
  
  
  |Causa|Consecuencia	|Tipo Exp.|	Cobertura| Cto. Rva|
  |:---:|---|---|---|--
  |3001 Despiste|3001 Daños Vehículo Asegurado|**DPM** |3001 Daños Propios| **1 Indemnización**
  |- |3002 Daños Vehículo Asegurado Honorarios|- |3001 Daños Propios| **2 Honorarios**

  El Expediente que se abra tendrá lo siguiente:

  |Tipo de Expediente|Cobertura|Concepto de Reserva
  |---|---|---|
  |DPM|  3001 Daños Propios|  1 Indemnización
  |--| 3001 Daños Propios| 2 Honorarios
  

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

