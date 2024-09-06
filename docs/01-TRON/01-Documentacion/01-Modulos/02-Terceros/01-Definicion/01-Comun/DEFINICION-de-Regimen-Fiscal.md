![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Regímenes Fiscales {#titulo}

## Contexto

El régimen fiscal es el conjunto de las normas e instituciones que rigen la situación tributaria de una persona física o jurídica. Se trata, por lo tanto, del conjunto de derechos y obligaciones que surgen del desarrollo de una determinada actividad económica.

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar los Códigos de los Regímenes Fiscales de los Terceros en un catálogo de información específico que se entrega a las entidades inicialmente vacío de contenido...

... De esta manera la entidad MAPFRE Local podrá emplear este atributo para efectuar una clasificación de uso propia y específica con los Terceros de la entidad.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición del Régimen Fiscal del Tercero.

### **Idioma**

Esta propiedad le indica al sistema el Idioma empleado en la definición del Régimen Fiscal en el Catálogo, como por ejemplo: español, inglés, Turco, ...

### **Código del Régimen Fiscal**

Esta propiedad indicará en el sistema el código del Régimen Fiscal de la Persona Física y/o Jurídica. 

### **Descripción del Régimen Fiscal**

Esta propiedad le indica al sistema cual es la denominación o descripción del Régimen Fiscal del Tercero, de acuerdo con el idioma utilizado en su definición.

A modo de ejemplo y en idioma *español*:

- Régimen de Incorporación Fiscal.
- Enajenación de bienes.
- Régimen de Actividades Empresariales con Ingresos a través de Plataformas Tecnológicas.
- Régimen de Arrendamiento.
- Régimen de Actividades Empresariales y Profesionales.
- ...

## Propiedades Operativas

### **Uso en Personas Físicas/Jurídicas**

Este atributo indica el Tipo de Terceros que puede utilizar el Código del Régimen Fiscal que se esté definiendo en el Sistema, siendo sus valores:

- personas Físicas. 
- personas Jurídicas. 
- *indistintamente* para unas y para otras.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica a NewTron si el código del Régimen Fiscal está inhabilitado para poder ser utilizado en las operaciones de captura y/o modificación del Tercero.

### **Fecha de Validez**

Esta propiedad le indica a NewTron la fecha a partir de la cual el Régimen Fiscal del Tercero estará plenamente operativo en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los categorías.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Regímenes Fiscales en el Sistema?

No existe una preferencia ni recomendación para establecer o estandarizar en el sistema su codificación si bien la entidad MAPFRE debe analizar la conveniencia de utilizar transversalmente en los procesos de la compañía este catálogo de información para su correcta definición y posterior explotación.

[Tabla TRON: DF_TPD_NWT_XX_TXR]:<>