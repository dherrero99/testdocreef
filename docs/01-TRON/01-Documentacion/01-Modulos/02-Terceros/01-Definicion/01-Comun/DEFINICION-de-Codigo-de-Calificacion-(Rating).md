![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Códigos de Calificación (Rating) {#titulo}

## Contexto

¿Qué son los **Códigos de Calificación** o (Ratings)?

El *Rating* es la calificación de solvencia de una Empresa o País para hacer frente a sus obligaciones financieras. Esta nota se la otorga una agencia especializada (Moody's, Fitch, Standard & Poor's,... ) que se conoce como agencia de Calificación.

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar los Códigos de Rating en un catálogo de información específico que se entrega a las entidades inicialmente vacío de contenido.

El sistema permite a nivel de compañía y por idioma (Español, Inglés,...) codificar estos códigos denominando e identificando individualmente cada una de ellos mediante una denominación o texto descriptivo, e.g:

| Código RATING.            |  Descripción            |
| -----------               | -----------             |
| 001                       | Grado Inversión Baa2    |
| 002                       | Grado Inversión Baa3    |
| 003                       | Grado Especulativo Ba1  |
| ...                       | ...                     |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema si el Código de Rating está inhabilitado para poder ser empleado en las operaciones de captura y/o modificación del Tercero persona Jurídica.

### **Fecha de Validez**

Esta propiedad le indica al Sistema la fecha a partir de la cual el código de Rating está plenamente operativo en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los cargos.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Códigos de Rating en el Sistema?

No existe una preferencia ni recomendación para establecer o estandarizar en el sistema su codificación si bien la entidad MAPFRE debe analizar la conveniencia de utilizar transversalmente en los procesos de la compañía este catálogo de información para su correcta y posterior explotación, e.g: 

- Agrupando y codificando los códigos de las diferentes Agencias de Rating que se van a usar en los procesos de la entidad
- Agrupando y codificando los códigos por tramos, e.g: del 000 al 99 para códigos de Moody's, del 200 al 299 para códigos de Fitch,...

[Tabla TRON: G1001304]:<>
