![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN Estructuras de Información Siniestros {#titulo}

<mark>Falta:</mark> Revisar Preguntas Frecuentes y Link a los documentos de agrupaciones y estructuras.

==EN CONSTRUCCIÓN==  

## **Objetivo**
La finalidad es definir toda la información que se va a solicitar en las diferentes operaciones del Módulo de Siniestros por Sector y Ramo.   
Si una estructura de información, por ejemplo, el __Relato del siniestro__, se va a solicitar en todos los sectores y en todos los ramos, se pondrá el sector genérico (9999-Todos los sectores) y el ramo genérico (999-Todos los Ramos).
Si se va a solicitar para todos los ramos de un sector, se pondrá el valor del sector y el valor del ramo será el genérico, para todos los ramos.  

Estas estructuras de información tendrán que estar definidas en el catálogo de estructuras y luego asociarlas a las diferentes agrupaciones (puntos de salto) donde se va a requerir esa información.

## **Propiedades Sector Ramo**

### **Sector**
Esta propiedad contendrá __[la clave del sector][sector]__ para el cual vamos a definir la estructura de información. 
Si la información se va para todos los sectores, se utilizará el genérico 9999- Todos los sectores.

[sector]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-de-Sector.md#titulo>

### **Ramo**
Este atributo indica la __[clave del Ramo][ramo]__ para el cual vamos a definir las estructuras de información.
Si la información se va para todos los ramos, se utilizará el genérico 999- Todos los ramos.

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>


### **Tipo de Expediente**
Este atributo sólo se pedirá en el caso de que la información sea para un __proceso a nivel de expediente__.   
Cuando sea de un proceso de siniestros, el sistema asignará el tipo de expediente genérico, que indica que es para todos los tipos de expedientes, si el proceso es de expedientes, habrá que introducir la __[clave del tipo de expediente][tipoexpediente]__. 

[tipoexpediente]: <../102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#titulo>

### **Agrupación de Información**

Los valores de este atributo ya están prefijados y los que afectan al módulo de siniestros que tienen que estar definidas en este catálogo son:  

#### Agrupaciones para __procesos de Siniestros__:
   -  __22__ Datos Fijos Siniestros **Antes de Consecuencias**  
   -  __2__ Datos Fijos del Siniestro **Después de Consecuencias**

#### Agrupaciones para __procesos de Expedientes__:
  - __4__ Complementarias de Expediente  

#### Agrupación para __Plan de Tramitación__: {#agrupacionplantramitacion}
  - __5__ Trámites  
   
#### Agrupación para __Salvamentos__:
  - __6__ Salvamentos  

#### Agrupación para __juicios__:
  - __20__ Juicios	  

#### Agrupación para __procesos de Liquidaciones__:
  - __23__ Liquidaciones

 [Definición Agrupaciones NO-LINK]

### **Estructura de Información**
Esta propiedad contendrá el código de la [estructura][estructura] de información que estamos definiendo para el sector ramo.  
Estas estructuras deberán estar definidas en el catálogo de estructuras y [asociada a las agrupación][agrupacion] que estamos definiendo.

 [estructura]:<NoLink> 
 [agrupacion]:<NoLink>

### **Número de Secuencia**
Este atributo indicará el __orden de presentación__ de la estructuras de información dentro del proceso. 
Se deberá definir en primer lugar la estructuras de información más comunes, más usadas.  


Ejemplos:
 
- Se quiere definir que para el **sector 3** y  el **ramo 300**, que en las operaciones de siniestros (apertura de siniestros, modificación de siniestros...), se pida la información siguiente: 

    |Sector|Ramo|Tipo Expediente|Agrupación|Estructura de Información|Secuencia|
    |---|---|---|---|---|--|
    |**3** (Autos) |**300** (Automóviles)|999 (Todos Tipos)| **2** Datos Fijos Siniestros|**1** Relato| 1
    |**3** (Autos) |**300** (Automóviles)|999 (Todos Tipos)| **2** Datos Fijos Siniestros|**2** Daños al Vehículo Asegurado| 2   
  |**3** (Autos) |**300** (Automóviles)|999 (Todos los Tipos)| **2** Datos Fijos Siniestros|**3** Lesionados Vehículo Asegurado| 3   

  El **número de secuencia** que se ha definido marcará el orden de presentación que se mostrará así:  

  1. Relato del siniestro
  2. Daños Vehículo Asegurado
  3. Lesionados Vehículo Asegurado
  4. etc.  

- Se quiere definir que para **sector 3** , para **todos los ramos**, para el tipo de expediente **DPM Daños Propios Materiales**, para las operaciones de expedientes, se pida como información complementaria el expediente:   

    |Sector|Ramo|Tipo Expediente|Agrupación|Estructura de Información|Secuencia|
    |---|---|---|---|---|--|
    |**3** (Autos) |**999** (Todos los Ramos)| **DPM** Daños Propios Materiales |**4** Complementarias de Expediente|**44** Profesionales que intervienen| 1
    |**3** (Autos) |**999** (Todos los Ramos)| **DPM** Daños Propios Materiales |**4** Complementarias de Expediente|**48** Plan de Tramitación| 1

### **Es obligatoria**
Esta propiedad indica si la información que se ha definido se va a pedir obligatoriamente. Las operaciones irán a esta tabla y primero mostrarán todas las estructuras de información que se haya definido como obligatorias (no se podrá salir de ellas sin grabar), y luego mostrarán todas las estructuras opcionales (No obligatorias), para que el usuario decida en cual entrar.

### **Lógica que determina si Es obligatoria**
Este atributo contendrá una lógica de Negocio, que determinará si la estructura de información es obligatoria o no, cuando no siempre sea si o no, si no que dependa de otros factores. 

Ejemplo:
Puede que haya información que dependiendo de la causa (origen del siniestro), sea obligatoria o no, o dependiendo si el siniestro se ha producido por un evento catastrófico...

### **Lógica que determina si se visualiza**
Esta propiedad o atributo, contendrá una lógica de Negocio que determinará si la estructura de información se visualiza o no se visualiza. Por ejemplo podemos determinar que la estructura que recoge la información del lesionado, sólo se muestre si se ha elegido la consecuencia de lesiones.
 
## **Vínculos**

## **Preguntas frecuentes**
- ¿Se pueden asociar a cada agrupación varias estructuras de información ?  
  Si se pueden elegir varias estructuras de información, pero habrá que indicar si son obligatorias u opcionales y en que orden se van a mostrar.  

  Cuando hay __varias estructuras obligatorias__, la operación las irá mostrando una a una por el orden de secuencia y no podrá salir sin haber grabado previamente los datos.  

  Cuando __hay una o varias estructuras no obligatorias u opcionales__, se mostrarán todas en el orden establecido para que el usuario elija que estructura quiere rellenas.


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
