![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Ramo Contable {#titulo}

## Objetivo

Los Ramos Contables no son sino unos códigos utilizados en la contabilidad que relacionan la **estructura técnica** de los Ramos Técnicos con la **estructura contable** de las entidades.

Esta relación se efectúa en el Sistema a nivel de Cobertura/Garantía por lo que previamente a la definición de las Coberturas en el sistema se definirán a nivel de entidad  la relación de posibles Ramos Contables que podrán ser utilizados posteriormente en la definición y configuración de las Coberturas.

Por otra parte, el sistema contempla poder parametrizar los Ramos contables de las Coberturas/Garantías de los Ramos Técnicos cuyo **Tratamiento de Emisión** corresponda a *Automóviles* de acuerdo a los Tipos de vehículos definidos y usados localmente por la entidad MAPFRE y que se puedan asociar al objeto asegurado Vehículo en la captura de su información durante el Proceso de Emisión.

- [Propiedades Generales](#propiedades-generales)
- [Propiedades Operativas](#propiedades-operativas)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo el Ramo Contable en el Sistema.

### **Sector**

Este atributo contiene el código del Sector de la compañía para el que se está definiendo el Ramo Contable en el Sistema.

### **Sub Sector**

Este atributo contiene el código de un Sub Sector definido y asociado al Código de Sector de la compañía para el que se está definiendo el Ramo Contable en el Sistema.

### **Ramo Contable**

Este atributo contiene el código del Ramo Contable en el Sistema compuesto por 9 posiciones que usualmente se conforman de la siguiente forma:

| Posiciones       | Descripción       |
| ----------       | -----------       |
| 1                | Sector            | 
| 2 - 3            | Sub Sector        |
| 4 - 5 - 6        | *Agrupamiento*    |
| 7 - 8 - 9        | Secuencia         |

### **Descripción del Ramo Contable**

Este atributo contiene la Descripción o Nomenclatura del Ramo Contable en el Sistema.

## Propiedades Operativas

### **Código Simplificado del Ramo Contable**

Este atributo contiene el código simplificado que facilita y permite recordar el Ramo Contable en el Sistema a efectos de agilizar su captura en el sistema.

### **Distribución de Saldos**

Este atributo contiene el tipo de distribución de Saldos contables en el sistema de acuerdo a las directrices marcadas por el Área de Administración y Finanzas de la entidad MAPFRE Local: Por Entidad, Sector, Sub Sector, Ramo Contable, 

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Estructura de Productos](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Estructura-Productos.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Ramos Contables en el Sistema?

Las posiciones correspondientes al *Agrupamiento* pueden definirse como cualquier secuencia que se estime conveniente por parte de la entidad local siendo la más usual aquella que identifica unívocamente el código del Ramo Técnico.

[Tabla TRON: G1002000]:<>