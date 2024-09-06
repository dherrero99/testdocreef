![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de las Entidades de Cobro y Pago de los Terceros {#titulo}

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar las diferentes Entidades de Cobro y Pago de los Terceros en un catálogo de información específico que se entrega inicialmente a las instalaciones vacío de contenido.

La definición de estas Entidades de Cobro y Pago en el Sistema se realiza por compañía e idioma (Español , Inglés, ...) pudiendo denominar e identificar individualmente cada una de ellas mediante una denominación o texto descriptivo.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición de la Entidad de Cobro y Pago de los Terceros.

### **Idioma**

Esta propiedad le indica al sistema el Idioma empleado en la definición de la Entidad de Cobro y Pago en el Catálogo, como por ejemplo: español, inglés,...

### **Código de la Entidad de Cobro y Pago**

Esta propiedad indicará en el sistema el código de la Entidad del Tercero de acuerdo al tipo de dato que sustentará la información en la Base de Datos.

### **Descripción de la Entidad de Cobro y Pago**

Esta propiedad le indica al sistema cual es la denominación o descripción de la Entidad del Tercero. 

A modo de **ejemplo** en idioma español:

| Código ENTIDAD            | Descripción           |
| -----------               | -----------           |
| 001                       | Banco Nacional        | 
| 010                       | Banco Extranjero      |
| ...                       | ...                   |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema que la Entidad de Cobro y Pago está inhabilitada para poder ser utilizada en las operaciones de captura y/o modificación del Tercero.

### **Fecha de Validez**

Esta propiedad le indica al Sistema la fecha a partir de la cual la Entidad de Cobro y Pago está plenamente operativo en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los cargos.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)
- [Medios de Cobro y Pago](./DEFINICION-de-Medio-de-Cobro-Pago.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de las Entidades de Cobro y Pago que pueden ser utilizadas en el Sistema?

No existe Corporativamente una preferencia o recomendación para establecer o estandarizar en el sistema su codificación.

[Tabla TRON: DF_THP_NWT_XX_ENT]:<>