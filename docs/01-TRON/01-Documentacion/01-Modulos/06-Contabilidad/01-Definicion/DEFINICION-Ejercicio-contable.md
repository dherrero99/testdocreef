![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: Falta: Revisar y completar objetivo, Ejemplos, imagenes, preguntas frecuentes**)

# DEFINICIÓN de Ejercicio contable 

## **Objetivo**
El objetivo es definir el periodo de tiempo en el que se realizarán las operaciones contables.

## **Propiedades**
### **Compañía**
Este atributo contiene el código de la compañía para la que se está definiendo el ejercicio contable.

### **Ejercicio**
Este atributo será la clave con la que se identifica el ejercicio contable.

Normalmente, si el ejercicio coincide con el año natural, se suelen utilizar como clave los dígitos del año, pero puede utilizarse cualquier otra codificación.

Ejemplo 

- Si hay un único ejercicio y coincide con el año  
  Ejercicio: 2023  

- Si hay más de un ejercicio en el mismo año  
  Ejercicio: 20231 (para el primer ejercicio)  
  Ejercicio: 20232 (para el segundo ejercicio)  

### **Fecha de apertura**
Este atributo indica la fecha en la que inicia el ejercicio contable.

Ejemplo  

- Si el ejercicio se inicia el primer día del año  
  Fecha de apertura: 01/01/2023

### **Fecha de cierre**
Este atributo indica la fecha en la que finaliza el ejercicio contable.

Ejemplo  

- Si el ejercicio coincide con el año natural  
  Ejercicio: 2023  
  Fecha de apertura: 01/01/2023  
  Fecha de cierre: 31/12/2023  

- Si el ejercicio está entre dos años naturales  
  Ejercicio: 2223  
  Fecha de apertura: 01/07/2022  
  Fecha de cierre: 30/06/2023  

- Si hay más de un ejercicio en el mismo año natural  

  1. Primer ejercicio  
    Ejercicio: 20231  
    Fecha de apertura: 01/01/2023  
    Fecha de cierre: 30/06/2023  
    
  2. Segundo ejercicio  
    Ejercicio: 20232  
    Fecha de apertura: 01/07/2023  
    Fecha de cierre: 31/12/2023  

### **Cierre**
Este atributo indica si el ejercicio contable está cerrado, es decir, no pueden realizarse más operaciones en este ejercicio.

El proceso de cierre puede ejecutarse varias veces, considerando que el ejercicio está cerrado definitivamente cuando este atributo así lo indica.  

### **Apertura definitiva**
Este atributo indica si el ejercicio está abierto definitivamente.

El asiento de apertura se puede ejecutar varias veces hasta que en este atributo se indique que la apertura es definitiva.

### **Inhabilitado**
Este atributo indica si el ejercicio está habilitado o no, para poder trabajar.

Un ejercicio inhabilitado no se puede utilizar, ni siquiera en consulta, es como si no existiera. 

## **Vínculos**
[DEFINICION de compañía](/docs/01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-producto/DEFINICION-Compania.md)

## **Preguntas frecuentes**
