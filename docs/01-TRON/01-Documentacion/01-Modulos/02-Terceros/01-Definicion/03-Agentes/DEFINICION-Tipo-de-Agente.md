![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de las Tipologías de Agentes/Intermediarios {#titulo}

## Contexto

Un *Cliente Distribuidor* es aquella persona o entidad jurídica que distribuye o podría distribuir productos aseguradores, financieros o servicios para MAPFRE o para alguna entidad competidora.

Cada país debe implementar una clasificación de clientes distribuidores homogénea que de servicio a las necesidades de negocio propias de la operación y que a su vez esté sincronizada con la Clasificación Corporativa del Cliente Distribuidor vigente.

A la hora de agrupar a los mediadores por fuentes de producción, hay ciertas características que se deben tener en cuenta y que deben cumplir con las definiciones corporativas aprobadas, definiciones que se realizan específicamente en la **Estructura de Clientes Distribuidores**. 

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de complementar la definición realizada en la Estructura de Clientes Distribuidores con la captura de una característica **adicional** en la definición de los Agentes, característica que puede determinar el nivel de granularidad necesario para *clasificar* la red comercial de acuerdo a las necesidades locales. 

A modo de ejemplo, este Atributo podría determinar ...

- Grado de Vinculación.
- Ubicación física.
- Canal de Origen: Tradicional, Digital, Telefónico.
- Oferta de Productos.
- Subvencionado o no.
- Ámbito: Global, Regional o Local.
- étc.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición del Tipo de Agente.

### **Tipo de Intermediario**

Esta propiedad indica el código del Tipo de Intermediario que se está capturando en el sistema.

### **Denominación del Tipo de Intermediario**

De acuerdo con el uso y explotación que se le vaya a dar localmente, este Atributo indicará la denominación o descripción de la Tipología del Agente o Intermediario, como por ejemplo:

| Tipo de Agente            |  Descripción               |
| -----------               | -----------                |
| 1                         | **Subvencionado**          |
| 2                         | **No Subvencionado**       |
| ...                       | ...                        |

o bien:

| Tipo de Agente            |  Descripción                           |
| -----------               | -----------                            |
| 1                         | **Oficina de Atención al Público**     |
| 2                         | **Oficina si Atención al Público**     |
| ...                       | ...                                    |

o bien:

| Tipo de Agente            |  Descripción          |
| -----------               | -----------           |
| 1                         | **MultiProducto**     |
| 2                         | **Especializado**     |
| 3                         | **MonoProducto**      |
| ...                       | ...                   |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema que el Tipo de Intermediario está inhabilitada para poder ser utilizada en las operaciones de captura y/o modificación del Agente.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)
- [Canales y Fuentes de Producción](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/05-Estructura-Canal-de-Distribucion/DEFINICION-Estructura-Canales.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de la Tipología de Intermediarios en el Sistema?

Se debe respetar la Identificación de los tipos de Intermediarios en el sistema de acuerdo con la Clasificación Operativa de los Clientes Distribuidores definida por el Área Corporativa de Negocio y CLientes.

[Tabla TRON A1001343 ]:<>