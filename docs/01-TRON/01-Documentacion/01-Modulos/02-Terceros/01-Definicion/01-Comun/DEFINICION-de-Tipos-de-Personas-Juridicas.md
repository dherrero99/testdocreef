![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de los Tipos de Personas Jurídicas {#titulo}

## Objetivo

El objeto de este catálogo es poder efectuar una clasificación de los Terceros Jurídicos.

- [Propiedades Generales](#propiedades-generales)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo el tipo de Persona Jurídica.

### **Idioma**

Esta propiedad le indica al sistema el Idioma empleado en la definición del Código del Consentimiento como por ejemplo: español, inglés, turco,...

### **Código del Tipo de Persona Jurídica**

Este atributo identifica en el sistema la clave de la Tipología del Tercero Jurídico.

### **Descripción del Tipo de Persona Jurídica**

Esta propiedad contiene la denominación o descripción de la clave del Tercero, de acuerdo con el idioma utilizado en la definición.

A modo de *ejemplo* y si el Idioma utilizado en la definición es el español:

| Tipo de Persona Jurídica | Descripción                     |
| :-----------:            | -----------                     |
| AAA                      | Corporación Int. Público        |
| BBB                      | Asociación Int. Público         |
| CCC                      | Fundación Int. Público          |
| 000                      | Empresa Int. **Privado**        |
| 001                      | Cooperativa Int. **Privado**    |
| 002                      | Sociedad Civil Int. **Privado** |
| ...

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que el Tipo de Persona Jurídica está inhabilitado para poder ser empleado en las operaciones de captura y/o modificación del Tercero.

### **Fecha de Validez**

Esta propiedad establece la fecha a partir de la cual la Tipología de la Persona Jurídica está disponible en el sistema para ser utilizada por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de las mismas para su posterior explotación.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Tipos de Personas Jurídicas en el Sistema?

Una práctica que se ha demostrado que funciona bien y por tanto se recomienda como modelo es utilizar las descripciones de las claves definidas para complementar la información de la tipología definida (en el ejemplo mostrado previamente se identifica si la Tipología del Tercero es de ámbito *público* o *privado* ), si bien la entidad MAPFRE debe analizar la mejor manera de utilizar transversalmente en los procesos de la compañía este catálogo de información para su correcta definición contemplando su posterior explotación. 

[Tabla TRON: DF_THP_NWT_XX_CGT con CGT_TYP_VAL =1]:<>