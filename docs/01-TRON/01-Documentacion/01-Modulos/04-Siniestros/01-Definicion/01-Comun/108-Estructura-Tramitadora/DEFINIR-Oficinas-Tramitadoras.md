![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN Oficinas Tramitadoras {#titulo}

==EN CONSTRUCCIÓN==  

## **Objetivo** 
La finalidad es definir aquellas __[oficinas][nivel3]__ (nivel3 de la estructura comercial), que van a poder tramitar siniestros.   
Las oficinas que estén definidas aquí, serán consideradas **_tramitadoras_**.  
Para cada oficina tramitadora habrá que definir su especialización.  
Cada supervisor y tramitador estará asociado a una oficina tramitadora.
 
[nivel3]:<../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/02-Estructura-Comercial/DEFINICION-Nivel3-Estructura-Comercial.md#titulo>

## **Propiedades**

### **Tratamiento**
Este atributo contendrá la clave del __[tratamiento][tratamientos]__ con el que puede trabajar la oficina tramitadora, es decir se está indicando al sistema que podrá trabajar con siniestros, cuya póliza tenga el tratamiento que estamos definiendo. 

Normalmente los tratamientos que se definen son:  

- Autos
- Diversos (Generales)
- Vida
- Transportes  

Se deberá definir tantas líneas como tratamientos en los que pueda trabajar la oficina tramitadora.

[tratamientos]:<../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-de-Tratamiento.md#titulo>

### **Sector**
Esta propiedad contendrá el __[sector][sector]__ con el que puede trabajar la oficina tramitadora, es decir se está indicando al sistema que podrá trabajar con siniestros, cuya póliza tenga el sector que estamos definiendo. 

Se podrá utilizar el sector Genérico 9999, que significará que esa tramitadora podrá trabajar con siniestros cuya póliza sea de cualquier sector.   

En el caso de que no trabaje en todos los sectores, se deberá definir tantas líneas como sectores en los que pueda trabajar la oficina tramitadora.  

[sector]:<../../../../../.././../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-de-Sector.md#titulo>

### **Ramo**
Esta propiedad contendrá el **[ramo][ramo]** con el que puede trabajar la oficina tramitadora, es decir se está indicando al sistema que podrá trabajar con siniestros, cuya póliza tenga el ramo que estamos registrando. 

Se podrá utilizar el **ramo Genérico 999**, que significará que esa tramitadora podrá trabajar con siniestros cuya póliza sea de cualquier ramo.   


En el caso de que no trabaje con todos los ramos, se deberá definir tantas líneas como ramos en los que pueda trabajar la oficina tramitadora.  

[ramo]:<../../../../../.././../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Nivel3 Tramitadora**
Esta propiedad contendrá la oficina tramitadora. Estas deberán estar existir como **[Nivel3][nivel3]** de la estructura comercial. Todas las propiedades que se van a definir serán para esta oficina tramitadora.


### **Tramita Juicios**
Esta propiedad indica si la oficina tramitadora va tratar **siniestros/expedientes** que estén en **juicios**.

### **Tramita Daños Personales**
Esta propiedad indica si la oficina puede tramitar **expedientes** cuya tipología sea **Daños Personales**.

### **Tramita Daños Materiales**
Esta propiedad indica si la oficina puede tramitar **expedientes** cuya tipología sea **Daños Materiales**.

### **Tramita Recobros de Salvamentos**
Esta propiedad indica si la oficina puede tramitar __[Salvamentos][recobros]__  (Recuperaciones Materiales). Los recobros tipo 'S'



### **Tramita Recobros de Recobros Económicos**
Esta propiedad indica si la oficina puede tramitar __[Recobros Económicos][recobros]__, los recobros tipo 'R'.


[recobros]:<../102-Tipo-de-Expediente/DEFINIR-Tipo-Expediente.md#tipo-de-recobro>

### **Tramita Pérdidas Totales**
Esta propiedad indica si la oficina puede tramitar expedientes que sean Pérdidas Totales.

Ejemplos:
 
- Se quiere definir que para tratamiento de **autos**, para el sector 3 y  el ***ramo 300**,  la tramitadora 1001, Tramita Juicios, Tramita Daños Personales..  


    |Tratamiento |Sector|Ramo|Tramitadora|Juicios|Daños Personales|...|
    |---|---|:---:|:---:|---|---|---|
    |A (Autos)|3 (Autos) |300 (Automóviles)| 1001 (Madrid Centro)|S|S|


- Se quiere definir que para tratamiento de **autos**, para **todos los ramos** del sector 3, **menos el ramo 300** ,la tramitadora 1001, Tramita Juicios..  


    |Tratamiento |Sector|Ramo|Tramitadora|Juicios|Daños Personales|...|
    |---|---|:---:|:---:|---|---|---|
    |A (Autos)|3 (Autos ) |999 (Todos)| 1001-(Madrid Centro)|S|N|..

- Se indica que para tratamiento de **vida**, para todos los sectores , para todos los ramos, la tramitadora 1001, Tramita Juicios ...

    |Tratamiento |Sector|Ramo|Tramitadora|Juicios|Daños Personales|...|
    |---|---|:---:|:---:|---|---|---|
    |V (Vida)|9999 (Todos ) |999 (Todos)| 1001-(Madrid Centro)|S|N|..

## Vínculos

## Preguntas frecuentes
- Para se utiliza esta definición  
    Por ejemplo para la re-asignación de un expediente que ha entrado en juicio, se consulta las oficinas tramitadoras que puedan tramitar juicios, para poder enviar el expediente.


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 


