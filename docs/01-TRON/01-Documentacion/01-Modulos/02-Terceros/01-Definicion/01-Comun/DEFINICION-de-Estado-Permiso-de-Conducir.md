![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de los Estados del Permiso de Conducir {#titulo}

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar las diferentes estados o situaciones en los que se pueden encontrar las licencias de conducción de las Personas Físicas en un catálogo de información específico que se entrega a las entidades **vacío de contenido**.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición del status del carnet de conducir del Tercero.

### **Código de Estado**

Esta propiedad le indica al Sistema si la información del Tercero asociado a la actividad contempla o no la existencia y generación de un código interno del Tercero.
A modo de ejemplo, 

| Status                |  Descripción    |
| -----------           | -----------     |
| 001                   | En Vigor        |
| CAD                   | Caducado        |
| 04A                   | Suspendido      |
| ...                   | ...             |

IMPORTANTE: No confundir la definición de este catálogo que contempla los posibles estados del carnet de conducir del Tercero, con los estados por los que pasa el proceso de **tramitación** del carnet o licencia de conducir.

### **Descripción del Estado de la Licencia de conducir**

Esta propiedad le indica al sistema cual es la denominación o descripción del status del carnet de conducir.

### **Abreviatura del Estado de la Licencia de conducir**

Esta propiedad le indica al sistema cual es la abreviatura del estado del carnet de conducir.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al sistema que el Código de Estado del Carnet de Conducir está inhabilitado para poder ser empleado en las operaciones de captura y/o modificación de la persona física.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

(1) ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación y uso de los posibles estados del Carnet de Conducir de las personas físicas en el Sistema?

No existe Corporativamente una preferencia o recomendación para establecer o estandarizar en el sistema su codificación en el sistema.

[Tabla TRON: G1001308]:<>