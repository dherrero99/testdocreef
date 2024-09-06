![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN Tipo de Causa {#titulo}
<mark>Falta:</mark> Preguntas y respuestas, Revisar si hago varios apartados 

==EN CONSTRUCCIÓN==  

## **Objetivo**
La finalidad es definir todas las __causas__ de todos los __procesos de siniestros__, incluidas las __causas origen del siniestro__.  
Se definirán las  causas por las que se modifica un siniestro, causas por las que se reabre un siniestro, causas por las que se realiza una peritación, causas de apertura de expedientes, causas por las que se modifica un expediente, etc.   

Habrá que definir tanto los atributos generales (utilizados por todos los ramos), como los atributos específicos para cada ramo.

## **Propiedades Generales Causas**
En este apartado se detallarán todos los atributos de las causas, comunes a todos los ramos, es decir los atributos que no cambian por ramo.  

### **Tipo de Causa**

Este atributo nos indicará el tipo de causa que se está definiendo.  
Hay que definir tanto las causas origen del siniestro, como las causas de los diferentes procesos del módulo de siniestros.  

Los __valores__ de este atributo ya están __prefijados__ y son estos:  

#### **Tipo de Causa Origen Siniestro** {#causaorigen}  
   - __1__: Causa del Siniestro (Origen)   

#### Tipos de Causas **Operaciones Siniestros** {#causasiniestros}  
  - __2__: Modificación de Siniestros   
  - __3__: Rehabilitación de Siniestros  
  - __9__: Terminación de Siniestros  

#### Tipos de Causas **Operaciones Expedientes** {#causaexpedientes}  

  - __15__: Apertura de Expedientes   
  - __4__: Modificación de Expedientes  
  - __19__: Cambio de Valoración  
  -  __5__: Rehabilitación de Expedientes  
  -  __6__: Terminación de Expedientes    

#### Tipos de Causas Operaciones **Liquidaciones** {#causaliquidaciones}  
  -  __7__: Rectificación de Liquidaciones  

#### Tipos de Causas Operaciones __Peritaciones__ {#causaperitaciones}  
  -  __8__: Causas de Peritación  
  - __16__: Resultado de la Peritación    


#### Tipos de Causas __Operaciones Juicios__ {#causajuicios}  
  - __10__: Reapertura del Juicio   

#### Tipos de Causas __Operaciones Facturación__ {#causafactura}  
  - __11__: Gastos No Amparados Facturación  

#### Tipos de Causas Operaciones __Control Técnico__ {#causacontroles}  

  - __12__: Rechazo Control Técnico Siniestro    
  - __14__: Rechazo Control Técnico Expediente  

#### Tipos de Causas __Operaciones Salvamentos__ {#causasalvamentos} 

  - __17__: Liberación Inventario Salvamentos  
  - __18__: Anulación del Inventario Salvamentos   


### **Causa**
Este atributo será la __clave__ por la que se va a identificar las distintas causas. Tanto las causas origen del siniestro, como las causas definidas para los distintos procesos del módulo de siniestros. 

Una clave podrá ser utilizada para uno o varios ramos.

### **Nombre de la Causa**
Este atributo será la __descripción de la clave__ definida para la causa. Puede contener números y/o letras. 

Ejemplos:

- Tipo de Causa: __1- Origen del siniestro__

  - Código de Causa: __1__ Nombre de la Causa: __Robo__  
  - Código de Causa: __2__ Nombre de la Causa: __Daños Por Agua__
  - Código de Causa: __3__ Nombre de la Causa: __Despiste__  

      
- Tipo de Causa: __2- Modificación del Siniestro__

  - Código de Causa: __1__ Nombre de la Causa: __Complementar Información__
  - Código de Causa: __2__ Nombre de la Causa: __Añadir un nuevo Lesionado__
  - Código de Causa: __3__ Nombre de la Causa: __Añadir un nuevo Perjudicado__


### **Nombre de la Causa para comunicaciones**
Este atributo será la descripción de la clave en el caso de que se quiera enviar una comunicación. 
Puede contener números y/o letras.  

Ejemplo: 

- Tipo de Causa: __9-Terminación del Siniestro__

  - Código de Causa: 1
  - Nombre de la Causa: No tiene las garantías contratadas
  - Nombre de Comunicación: __El siniestro no puede ser cubierto ya que no entra dentro de las garantías contratadas en su póliza.__

### **Es Tramitable**
En este atributo indicará si la causa que se está definiendo, se va a utilizar en la tramitación de siniestros.   

Cuando la causa es del tipo:  

__Tipo 1__- Origen de Siniestros

- Si este atributo es __afirmativo__, le indicará al sistema que el siniestro puede continuar registrándose y se podrán abrir expedientes.  

- Si este atributo es __negativo__, le indicará al sistema que no se pueden pedir las consecuencias, ni abrir expedientes, hasta que no se cambie a una causa tramitable.

__Resto Tipos de Causas__ (Tipo 2.- Modificación del siniestro, Tipo 3.- Rehabilitación de siniestros, etc.)

- Si el atributo indica que __es Tramitable__, el usuario podrá seleccionar dicha causa cuando el proceso lo requiera. 

- Si el atributo indica que __no es tramitable__ se utilizará para casos extraordinarios, como procesos automáticos.

Ejemplos:

- Tipo Causa: __1-Origen del Siniestro__   

  - Causa: __8__, Nombre: __Pendiente de Investigación__, Tramitable: __N__  
  - Causa: __9__, Nombre: __Desconocida__, 		        Tramitable: __N__    
  
- Tipo Causa: __4 -Terminación del Siniestro__
  - Causa: __9999__ Nombre: __Terminación Automática__, Tramitable: __N__  
   

- Tipo Causa: __3-Rehabilitación del Siniestro__

  - Causa: __9999__ Nombre: __Rehabilitación Automática__, Tramitable: __N__  


En el ejemplo, el tipo de Causa, 4 y 5, no podrá ser seleccionada por el usuario, son causas utilizadas por los procesos automáticos. 

### **Inhabilitada**

Este atributo indica si la causa que está definida, está habilitada para poder ser asociada a un ramo, o por el contrario, ya no está habilitada para poder ser utilizada en la definición de causas por Ramo. Las causas inhabilitadas, no se mostrarán para poder ser asociadas.

## **Propiedades Causas por Ramo** {#propiedadesramo}
Como se ha indicado anteriormente, las causas están definidas a nivel de compañía, y estas podrán ser definidas para ser utilizadas dentro de un ramo o no. En este apartado se detallará todos los atributos necesarios para definir el comportamiento de la causa dentro de un Ramo.   

### **Ramo**
Este atributo indica la __[clave del Ramo][ramo]__ al que se va a asociar las causas definidas previamente a nivel de compañía.  

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Tipo de Expediente**
Este atributo sólo se pedirá en el caso de que el tipo de causa sea para un __proceso a nivel de expediente__. Cuando sea de un proceso de siniestros, el sistema asignará el tipo de expediente genérico, que indica que es para todos los tipos de expedientes. Si la causa es a nivel de expediente, habrá que introducir la **[clave del tipo de expediente][tipoexpediente]**

[tipoexpediente]: <./DEFINIR-Tipo-Expediente.md#titulo>

### **Lógica para validar la causa** {#logicaparavalidarlacausa}
Este atributo contendrá una lógica de Negocio, que podrá realizar validaciones extras en función de información introducida o información propia de la instalación.

Ejemplo:

Cuando se está capturando la causa del siniestro (Tipo 1- Origen del siniestro), para el que se está definiendo, al seleccionar la causa del siniestro se puede validar que, si se ha introducido un evento catastrófico, no se puedan elegir ciertas causas.

### **Número de Secuencia** {#numerodesecuencia}
Este atributo indicará el __orden de presentación__ de las causas. Se intentará presentar en primer lugar las causas más comunes, más usadas.

### **Inhabilitada**
Este atributo indica si la causa que está definida, está habilitada para poder ser utilizada o, por el contrario, ya no está habilitada para poder ser usada. Las causas inhabilitadas, no se mostrarán para poder ser seleccionadas.

## **Vínculos**

## **Preguntas frecuentes**
- ¿Qué tipos de causas son las que luego se van asociar a las causas consecuencias?  
  Solamente las causas de tipo __1__ Origen deL siniestro. El resto de causas son sólo para las operaciones de siniestros.

- ¿Se van a poder seleccionar varias causas?  
  En todos los tipos de causas (Apertura de expedientes, Modificación de Siniestros...),se van a poder seleccionar varias causas, excepto en el tipo de causa __1- Origen del Siniestro__, que sólo se podrá elegir una única causa.

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
