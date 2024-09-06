![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de los Tipos de Token en los Medios de Cobro o Pago {#titulo}

## Contexto

La acción de 'crear un toquen (Token)' en la Tesorería es el proceso de reemplazar el número de cuenta tradicional de una tarjeta de pago con un toquen (Token) o ficha digital en las transacciones en línea y con dispositivos móviles conservando la información de los datos de la Tarjeta pero sin comprometer su seguridad. 

El toquen se puede restringir para utilizar con un dispositivo móvil, comercio o tipo de transacción específico.

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar los tipos de tóquenes que se pueden utilizar en los medios de Cobro y Pago de los Terceros, en un catálogo de información específico que se entrega inicialmente a las instalaciones vacío de contenido.

La definición de los tipos de tóquenes utilizados en los Medios de **Cobro** / **Pago** en el Sistema se realiza por compañía e idioma (Español , Inglés, ...) pudiendo denominar e identificar individualmente cada una de ellos mediante una denominación o texto descriptivo, e.g:

| Tipo de TOQUEN            | Descripción           |
| -----------               | -----------           |
| 001                       | VISA                  | 
| 010                       | MASTERCARD            |
| CCC                       | APPLE PAY             |
| ...                       | ...                   |

## Propiedades Operativas

### **Toquen Real o Toquen Generado**

Esta propiedad le indica al sistema si el Toquen es una ficha Real o es en cambio un toquen generado automáticamente.

### **Secuencia para generar el Toquen**

Esta propiedad le indica al sistema el código de la secuencia ORACLE que se ha de ejecutar para generar el Toquen.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema que el tipo de Toquen está inhabilitada para poder ser utilizada en las operaciones de captura y/o modificación del Tercero.

### **Fecha de Validez**

Esta propiedad le indica al Sistema la fecha a partir de la cual la Tipología del Token de los Medios de Cobro o Pago está plenamente operativo en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los cargos.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de las tipologías de los Tóquenes que pueden ser utilizadas en el Sistema?

No existe Corporativamente una preferencia o recomendación para establecer o estandarizar en el sistema su codificación.

[Tabla TRON: DF_THP_NWT_XX_TKD]:<>