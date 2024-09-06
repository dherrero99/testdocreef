![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Primer Nivel de la Estructura de Canales {#titulo}

## Contexto

La Configuración de los Clientes Distribuidores, de acuerdo con la Clasificación Corporativa se realiza en el **primer nivel** de la estructura de canales.

- [Propiedades Generales](#propiedades-generales)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo el Cliente Distribuidor en el sistema.

### **Código del Primer Nivel**

Este atributo identifica la clave que identificará al Primer Nivel de la estructura de canales en el Sistema.

La clasificación de clientes distribuidores **Corporativa** contempla los siguientes tipos de clientes distribuidores:

- *Directo*: personas, normalmente empleados, o medios de distribución que realizan ventas para MAPFRE sin percibir una retribución variable directa a cambio.

- *Red Propia/Red Agencial*: personas u organizaciones que se dedican a la venta de seguros como actividad principal o complementaria y que distribuyen en exclusividad para MAPFRE.

- *Red Externa/Corredores*: individuos u organizaciones que se dedican a la venta de seguros como actividad principal o complementaria y que distribuyen para varias compañías de seguros.

- *Bancario*: entidades bancarias, cooperativas de crédito al consumo, producción proveniente de operaciones societarias con socios bancarios y cualquier otra persona u organización que desarrolle su actividad comercial en el entorno de oficinas bancarias o los sistemas de distribución de estas entidades.

- *Acuerdos*: acuerdos de distribución con organizaciones cuya principal actividad económica no es la venta de seguros y cobran una comisión por acceder al cliente final bien a través de su estructura de distribución, o cediendo la explotación de la cartera a MAPFRE.

### **Descripción del Primer Nivel**

Esta propiedad contiene la denominación o descripción de la clave del Primer Nivel de la estructura de Canales.

### **Abreviatura del Primer Nivel**

Este Atributo contiene la denominación o descripción de la clave del Primer Nivel de la estructura de Canales en formato abreviado.

A modo de *ejemplo* la estructura propuesta es:

| Clave del Primer Nivel  | Descripción              | Abreviatura  |
| :-----------:           | :-----------             | :------      |
| 01                      | Directo                  | Dir.r        |
| 02                      | Red Propia - Agencial    | Prop.        |
| 03                      | Red Externa - Corredores | Ext.         |
| 04                      | Bancario                 | Ban.         |
| 05                      | Acuerdos                 | Acu.         |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que el Tipo de Cliente Distribuidor está inhabilitado para poder ser utilizado en la asignación a los Agentes.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

1. ¿Existe alguna premisa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Clientes Distribuidores en el Sistema?

    No es posible alterar la codificación preestablecida en el sistema para este Nivel de la Estructura de Canales.

## Audiencia

  - negocio
  - analista
  - implementador
  - desarrollador

El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#elemento>
[Poliza]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#poliza>

[Tabla TRON: A1000721]:<>