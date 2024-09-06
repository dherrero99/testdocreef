![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Oficinas Habilitadas por Agente {#titulo}

## Contexto

Un *cuadro de comisiones* es un concepto empleado en la configuración del sistema cuyo significado es relacionar y estructurar bajo una misma clave características heterogéneas (de la estructura comercial, de la estructura de Canales, del Cliente, ...) para obtener los porcentajes a aplicar en el cálculo de los importes de las comisiones.

## Objetivo

El objetivo es **asignar y asociar** a los Agentes la/s clave/s de los Cuadros de Comisiones que son de aplicación en el cálculo de las comisiones del Proceso de Emisión de las pólizas y suplementos intermediados por ellos y de acuerdo con la definición de los atributos de cálculo de comisiones que se especifican en la configuración de los Ramos.

- [Propiedades Generales](#propiedades-generales)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía en la que se está asociando al agente el cuadro de comisiones.

### **Clave de Agente**

Esta propiedad identifica la clave del intermediario de acuerdo con la configuración de las mismas previamente establecidas.

### **Código de Tratamiento de Emisión**

Este atributo identifica en el sistema la clave del tratamiento de Emisión de acuerdo con la configuración realizada en la estructura de productos de la entidad.

### **Cuadro de Comisiones**

Este atributo identifica en el sistema la clave del cuadro de comisiones.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que la Clave del Cuadro de Comisiones está inhabilitada para poder ser empleada para su utilización en el Sistema.

### **Tipo de Inhabilitación**

Esta propiedad establece si la inhabilitación del Cuadro de Comisiones va a afectar únicamente a las pólizas de **Nueva Producción** o afecta tanto a los **Movimientos de Nueva Producción** como a los suplementos emitidos sobre ellas o **Movimientos de Cartera**.

### **Fecha de Validez**

Esta propiedad establece la fecha a partir de la cual la asociación Agente/Cuadro de Comisiones está disponible en el sistema para ser utilizada por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones configuradas.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Estructura de Productos](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Estructura-Productos.md#titulo)
- [Configuración de Ramos](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#propiedades-relacionadas-intermediarios-comisiones)
- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna aclaración operativa que deba ser tomada en consideración localmente en la asignación de los cuadros de comisiones a los agentes?

Una práctica que se ha demostrado que funciona bien y por tanto se recomienda como modelo es utilizar las descripciones de las claves definidas para 'mostrar' algo más de información, si bien la entidad MAPFRE debe analizar la mejor manera de utilizar transversalmente en los procesos de la compañía este catálogo de información para su correcta definición contemplando su posterior explotación. 

**(2)** No confundir un **Cuadro de Comisiones** con un **Cuadro de Distribución de Comisiones**

**(3)** Diferencia del término **Nueva Producción** vs. **Cartera**

Atendiendo al momento temporal en el que se generan las comisiones en el proceso de emisión, puede establecerse la siguiente clasificación:

- Comisiones de nueva producción. Para distinguirlas de la comisión de cartera, se da ese nombre a la que se percibe exclusivamente durante el primer año de vigencia de la póliza (Generalmente y a fin de estimular la labor de captación de nuevas operaciones, este tipo de comisión suele ser de importe más elevado que la de cartera).

- Comisiones de cartera. Para distinguirla de la comisión de nueva producción, se da este nombre a la que tiene su origen en la cartera de quien la percibe (pólizas vigentes en años sucesivos). Esta comisión existe mientras tengan vigencia las pólizas suscritas a través de la gestión comercial del agente.

## **Audiencia**

  - [negocio]
  - [analista]
  - [implementador]
  - [desarrollador]

 
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#elemento>
[Poliza]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#poliza>

[Tabla TRON: ]:<>