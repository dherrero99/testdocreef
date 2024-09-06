![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Consentimientos {#titulo}

- [Propiedades Generales](#propiedades-generales)
- [Propiedades Operativas](#propiedades-operativas)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

Se entiende por consentimiento «toda manifestación de voluntad, libre, inequívoca, específica e informada, mediante la que el interesado acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen».

Funcionalmente el núcleo del Sistema cuenta con la posibilidad de identificar y definir en un catálogo de información específico que se entrega a las entidades **vacío de contenido**, los diferentes Consentimientos que se pueden asociar a los Terceros en la captura o modificación de sus datos.

... De esta manera la entidad MAPFRE estará en disposición de tratar y explotar adecuadamente esta información de acuerdo a sus necesidades específicas.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición del Consentimiento del Tercero.

### **Idioma**

Esta propiedad le indica al sistema el Idioma empleado en la definición del Código del Consentimiento como por ejemplo: español, inglés,...

### **Código del Consentimiento**

Esta propiedad indicará la clave del Consentimiento que se está definiendo en el Sistema pudiendo agrupar bajo un mismo código distintos Tipos de Consentimiento.

### **Descripción del Consentimiento**

Esta propiedad le indica al sistema la denominación o nombre del Consentimiento que se está definiendo. 

## Propiedades Operativas

### **Tipo del Consentimiento**

Este Atributo que está asociado al Código del Consentimiento e indirectamente al Tercero como parte de su información, indica en el Proceso de Relación con el Cliente sobre qué procedimiento/s se podrá incluir o excluir al Tercero cumpliendo así con su mandato.

En idioma español la relación de tipos que provee el núcleo es:

- Publicidad.
- Comunicaciones Comerciales en formato Electrónico.
- Cesión de Datos.
- Analítica de Clientes.
- Perfilado.
- Transferencia.
- Internacionalidad.
- Fidelización.
- Envío.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema que la definición del Código del Consentimiento está inhabilitada para poder ser utilizada en las operaciones de captura y/o modificación del Tercero.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de los Códigos de Consentimiento de los Terceros en el Sistema?

Es `obligatorio` *respetar* los valores de los Tipos de Consentimientos habilitados en el Sistema.

[Tabla TRON: DF_TPD_NWT_XX_COE]:<>