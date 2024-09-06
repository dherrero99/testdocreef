![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Tipos de Documentos Identificativos de Terceros {#titulo}

## Contexto

En los diferentes procesos que se circunscriben en la actividad propia de una Entidad Aseguradora es necesario identificar inequívocamente a las distintas personas físicas y/o jurídicas que de una u otra forma interactúan con la entidad, siendo así que para cada una de ellas la identificación se realizará mediante el uso de un Tipo de Documento y un Código único asociado a este.

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar los distintos Tipos de Documentos Identificadores de los Terceros, sean estos personas Físicas o Jurídicas, en un catálogo de información específico que se entrega a las entidades vacío de contenido.

La definición de las Tipologías de los Documentos que identificarán a los Terceros en el sistema se realiza a nivel de la compañía pudiendo definir y denominar individualmente cada uno de ellos mediante una clave y una denominación o texto descriptivo, e.g:

| Tipo de Documento         |  Descripción                       |
| -----------               | -----------                        |
| **NIF** - España          | Número de Identificación Fiscal    |
| **DNI** - España          | Documento Nacional de Identidad    |
| **RFC** - México          | Registro Federal de Causantes      |
| **RUT** - Chile           | Rol Único Tributario               |
| **RUT** - Colombia        | Registro único Tributario          |
| **TIN** - Malta           | Tax Identification Number          |

## Propiedades Operativas

### **Uso en Personas Físicas**

Este atributo indica si la Tipología del Documento identificador se usa para personas Físicas, para personas Jurídicas o indistintamente para unas u otras.

`NOTA:`En el supuesto que la Tipología del Documento se utilice indistintamente para personas físicas y jurídicas este atributo debe dejarse sin valor en su definición.

### **Real**

Este atributo indica si la Tipología del Documento identificador es o no un tipo de documento real. 

### **Documento Alternativo**

Este atributo indica si la Tipología del Documento identificador es usado para identificar al Tercero de manera alternativa, e.g:

| Tipo de Documento          |  Valor              |
| -----------                | ------------------- |
| **NIF** - Nro. Id. Fiscal  | 50818773A           |
| **NUU** - NUUMA            | JUANPE              |
| **TEC** - TeCuidamos       | 57732-05-2022       |

Lo habitual sería identificar a Juan Pérez Pérez con el tipo de documento ‘NIF’ y con el código 50818773A, si bien, el sistema también permite identificar alternativamente a esta persona física con los otros dos tipos de documentos definidos como documentos alternativos ‘NUU’ y ‘TEC’.

De esta manera podremos llegar a conocer el NIF de Juan Pérez Pérez partiendo de la Clave del Número único de MAPFRE o de la clave de TeCuidamos por estar los tres registros relacionados entre sí.

`NOTA:` La captura de los documentos Alternativos no está permitida en los procesos de Gestión de Pólizas y Contratos y Gestión de Siniestros y Prestaciones.

### **Generación Automática**

Esta propiedad le indica al sistema si el código del documento asociado a la tipología definida se generará o no de forma automática en el proceso de captura de información del Tercero.

`NOTA:` En el supuesto que se haya definido que el código del documento se ha de generar automáticamente, es necesario que la Dirección de Tecnología local defina e identifique el nombre de la secuencia Oracle a ser utilizada.

## Otras Propiedades

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de las tipologías de documentos en el Sistema?

Corporativamente no existe una preferencia ni recomendación para establecer o estandarizar en el sistema la codificación de los Tipos de Documentos Identificadores.

[Tabla TRON: A1002300]:<>