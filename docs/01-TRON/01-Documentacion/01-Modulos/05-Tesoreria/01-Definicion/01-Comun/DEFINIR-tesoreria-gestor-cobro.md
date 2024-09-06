![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: completar objetivo, Ejemplos, imagenes, preguntas frecuentes**)

# DEFINICIÓN de Gestor de cobro {#titulo}

## **Objetivo**
El objetivo es identificar los distintos tipos de gestores de cobro permitidos.

Se pueden crear tipos de gestores de cobro asociados a la clasificación estandar de la aplicación, de forma que su comportamiento ya está preestablecido, o crear nuevos tipos de gestores con una clasificación distinta a la estandar, de manera que será necesario establecer la forma de trabajar con dicho tipo de gestor.

## **Propiedades**
### **Compañía**
Este atributo contiene el código de la compañía para la que se está definiendo el tipo de gestor de cobro.

### **Tipo de gestor**
Este atributo contiene el tipo de gestor de cobro que se está definiendo, será con el que se identifique el tipo de gestor en la aplicación.

Ejemplo:
- Tipo de gestor: AG
- Tipo de gesgor: BA

### **Nombre de tipo de gestor**
Este atributo contiene la descripción del tipo de gestor que se está definiendo.

Ejemplo:  
- Tipo de gestor: AG  
Nombre de tipo de gestor: Agente

- Tipo de gestor: BA  
Nombre de tipo de gestor: Banco

### **Clase de gestor**
Este atributo contiene la clasificación del gestor.

Los valores estándar podrán ser:

- 1: AGENTE   
- 2: BANCO  
- 3: COBRADOR  
- 4: DÉBITO AUTOMATICO EN CUENTA  
- 5: GESTOR DIRECTO  
- 6: GESTOR PILOTO COASEGURO  
- 7: OFICINA COMERCIAL  
- 8: DEBITO CON TARJETA DE CREDITO  
- 10: GESTOR DE IMPAGOS

Esta clasificación es la que determina el comportamiento del gestor dentro de la aplicación. 

Si el atributo contiene un valor que no esté dentro de la clasificación anterior, indica que no es un gestor estándar.

Ejemplo:  
- Tipo de gestor: AG  
Nombre de tipo de gestor: Agente  
Clase de gestor: 1 (AGENTE)

- Tipo de gesgor: BA  
Nombre de tipo de gestor: Banco  
Clase de gestor: 2 (BANCO)

- Tipo de gestor: EX  
Nombre de tipo de gestor: Cobrador especial externo  
Clase de gestor: 9 (no es un gestor estándar)

### **Programa**
Este atributo contiene la lógica de negocio que obtiene la relación de tipos de gestores de cobro según su clasificación. 

### **Programa valida**
Este atributo contiene la lógica de negocio que valida el tipo de gestor de cobro, cuando no está clasificado dentro del estándar. 

## **Vínculos**
[DEFINICION de compañía](/docs/01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-producto/DEFINICION-Compania.md)

## **Preguntas frecuentes**
