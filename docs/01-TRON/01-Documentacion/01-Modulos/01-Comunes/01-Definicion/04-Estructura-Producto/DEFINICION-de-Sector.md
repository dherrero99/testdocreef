![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Sectores {#titulo}

## Objetivo

Un Sector es una clave de agrupación o clasificación de Ramos con características técnicas similares que permite realizar de una manera estructurada el análisis de los Ramos de la entidad y el estudio de la composición de la Cartera de las pólizas que los conforman, sea este para un uso interno y/o externo.

- [Propiedades Generales](#propiedades-generales)
- [Propiedades Operativas](#propiedades-operativas)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo el Sector.

### **Sector**

Esta propiedad identifica la clave del Sector que estemos configurando en el Sistema.

### **Descripción del Sector**

Esta propiedad contendrá la denominación o descripción del Sector.

### **Descripción Abreviada del Sector**

Esta propiedad contiene la denominación o descripción abreviada del Sector definido.

A modo de *ejemplo*, una Entidad podría definir los siguientes Sectores:

| Clave del Sector        | Descripción         | Abreviatura.   |
| :-----------:           | :-----------        | :--------      | 
| 0001                    | Vida                | Vid.           |
| 0002                    | No Vida             | No Vid.        | 

... o bien ...

| Clave del Sector   | Descripción         | Abreviatura.   |
| :-----------:      | :-----------        | :--------      | 
| 0001               | Automóviles         | Autos          |
| 0002               | multi-riesgo        | Mult.          | 
| 0003               | Salud               | Salud          | 
| 0004               | Resto No Vida       | Resto No Vid.  | 
| ...                | ...                 | ...            |

## Propiedades Operativas

### **Marca Emisión**

Si esta propiedad está activada en el Catálogo de Definición, el Sistema establecerá que la clave del Sector se puede emplear y asociar en la definición de los Ramos.

`NOTA`: Solamente puede existir un registro con esta marca no activa.

### **Número de Pólizas Reservadas**

Este Atributo del catálogo de definición de los Sectores, establece el número de pólizas que se generan automáticamente en el sistema con su codificación definitiva.

### **Número de Presupuestos Reservados**

Este Atributo del catálogo de definición de los Sectores, establece el número de presupuestos que se generan automáticamente en el sistema con su codificación definitiva.

### **Estadísticas**

Si esta propiedad está activada en el Catálogo de Definición, el Sistema establecerá que la obtención de las estadísticas y reportes deben realizarse o bien por subsector o bien por Modalidad o Producto Comercial.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Configuración de Subsectores](./DEFINICION-de-SubSector.md#titulo)
- [Configuración de Ramos/Productos](./DEFINICION-Ramo-Tecnico.md#titulo)
- [Numeración y Reserva de Pólizas](../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/01-Definicion/01-Comun/104-Numero-de-poliza/DEFINICION-Formato-numero-poliza.md#titulo)
- [Numeración y Reserva de Presupuestos](../../../../NOLINK.md)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Sectores en el Sistema?

Los más habitual es codificar sus claves de acuerdo con las normas, usos y procedimientos de la Asociación o entidad que represente localmente la industria aseguradora y a la que haya que proveer regularmente de información estadística.

## **Audiencia**

  - [negocio]
  - [analista]
  - [implementador]
  - [desarrollador]

[Referencia a los términos]  
 
[Elemento]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#elemento>
[Poliza]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos-Comunes.md#poliza>

[Tabla TRON: A1000200]:<>