![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Categorías {#titulo}

## Contexto

Se denomina categoría a una clase, un tipo, una condición o una división de algo.

Conceptualmente y en el ámbito de las personas Físicas, su categorización permite conformar grupos de personas de acuerdo a sus capacidades, responsabilidades, antigüedad en el puesto, actividades profesionales, grupo social al que pertenece, ... 

... mientras que en el ámbito de las personas jurídicas permite aglutinar entidades de acuerdo a su personalidad jurídica, o bien referidas a las clasificaciones de las personas jurídicas en la Administración Pública, de acuerdo al tipo de derecho público o privado que las amparan,...

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar los Códigos de Categorías en un catálogo de información específico que se entrega a las entidades inicialmente **vacío de contenido.**

... De esta manera la entidad MAPFRE Local podrá emplear este atributo para efectuar una clasificación de uso propio y específico con los Terceros de la entidad.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición de la Categoría del Tercero.

### **Idioma**

Esta propiedad le indica al sistema el Idioma empleado en la definición de la Categoría en el Catálogo, como por ejemplo: español, inglés,...

### **Código de la Categoría del Tercero**

Esta propiedad indicará en el sistema el código de la Categoría del Tercero. 

### **Descripción de la Categoría del Tercero**

Esta propiedad le indica al sistema cual es la denominación o descripción de la Categoría del Tercero, de acuerdo con el idioma utilizado en la definición.

A modo de ejemplo y si el Idioma utilizado en la definición es el español:

| Código Categoría         | Descripción               |
| -----------              | -----------               |
| 01                       | Categoría 1.              | 
| 02                       | Categoría 2               |
| 03                       | Categoría 3               |
| ...                      | ...                       |

## Propiedades Operativas

### **Uso en Personas Físicas**

Este atributo indica si la Tipología de la categorización del Tercero se usa para **personas Físicas**, para **personas Jurídicas** o **indistintamente** para unas u otras.

`NOTA` : En el supuesto que el código de la Categoría se pueda utilizar indistintamente tanto para personas físicas como para personas jurídicas, este atributo debe dejarse sin valor/en blanco en su definición.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema si la calidad está inhabilitada para poder ser utilizada en las operaciones de captura y/o modificación del Tercero.

### **Fecha de Validez**

Esta propiedad le indica al Sistema la fecha a partir de la cual la clase del Tercero está plenamente operativa en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los categorías.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Categorías en el Sistema?

No existe una preferencia ni recomendación para establecer o estandarizar en el sistema su codificación si bien la entidad MAPFRE debe analizar la conveniencia de utilizar transversalmente en los procesos de la compañía este catálogo de información para su correcta definición contemplando su posterior explotación.

[Tabla TRON: DF_TPD_NWT_XX_CST_CTG]:<>