![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Sub-Sectores {#titulo}

## Objetivo

Un Sub-Sector es una agrupación o clasificación de Ramos con características técnicas similares como subconjunto de la totalidad de los Ramos que conforman el Sector de Seguros al que pertenece.

- [Propiedades Generales](#propiedades-generales)
- [Propiedades Operativas](#propiedades-operativas)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo el Sub-Sector.

### **Sector**

Esta propiedad identifica la clave del Sector al que está asociado y del que depende el Sub-Sector. 

### **Sub-Sector**

Este atributo identifica en el sistema la clave del Sub-Sector.

### **Descripción del Sub-Sector**

Esta propiedad contiene la denominación o descripción del Subsector que se esté configurando en el catálogo.

### **Descripción Abreviada del Sub-Sector**

Esta propiedad contiene la denominación o descripción abreviada de la Clave del Sub-Sector.

A modo de *ejemplo*, podemos definir los siguientes Subsectores asociados al Sector **Resto Ramos No Vida**:

| Clave del Sub-Sector    | Descripción              | Abreviatura.   |
| :-----------:           | :-----------             | :--------      | 
| 0001                    | Accidentes               | Acc.           |
| 0002                    | Incendios                | Inc.           | 
| 0003                    | Otros Daños a los Bienes | Otros          | 
| 0004                    | Multi-riesgos            | Mult.          | 
| ...                     | ...                      | *...*          |

## Propiedades Operativas

### **Marca Emisión**

Si esta propiedad está activada en el Catálogo de Definición, el Sistema establecerá que la clave del Sub-Sector se puede emplear y asociar en la configuración de los Ramos.

`NOTA`: Solamente puede existir un registro con esta marca no activa.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Definición de Sectores](./DEFINICION-de-Sector.md#titulo)
- [Configuración de Ramos/Productos](./DEFINICION-Ramo-Tecnico.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación que deba ser contemplada localmente en la codificación, uso y definición del catálogo de Sub-sectores en el Sistema?

Los más habitual es codificar sus claves de acuerdo con las normas, usos y procedimientos de la Asociación o entidad que represente localmente la industria aseguradora y a la que haya que proveer regularmente de información estadística con este nivel de detalle.

## **Audiencia**

  - [negocio]
  - [analista]
  - [implementador]
  - [desarrollador]

[Referencia a los términos]  
 
[Elemento]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#elemento>
[Poliza]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#poliza>

[Tabla TRON: A1000250]:<>