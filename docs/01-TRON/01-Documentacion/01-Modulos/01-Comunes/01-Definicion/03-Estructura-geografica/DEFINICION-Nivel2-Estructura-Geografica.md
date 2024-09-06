![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Segundo Nivel de la Estructura Geográfica {#titulo}

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar los segundos niveles de la estructura Geográfica en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

### **Código del Primer Nivel**

Este atributo contiene la clave que identificará al Primer Nivel de la estructura Geográfica al que pertenecerá la clave del segundo Nivel de la estructura que se esté configurando.

### **Código del Segundo Nivel**

Este atributo identifica específicamente la clave que identificará al Segundo Nivel de la estructura Geográfica que estará asociada en el catálogo a la clave del primer nivel de la estructura.

### **Descripción del Segundo Nivel**

Esta propiedad contiene la denominación o descripción del Segundo Nivel (Descripción que debería estar en coherencia con el idioma utilizado en la definición del primer nivel de la estructura al que está asociado).

### **Descripción Vernácula del Segundo Nivel**

Esta propiedad contiene la denominación o descripción del Segundo Nivel de la Estructura Geográfica de acuerdo con el idioma vernáculo.

### **Abreviatura del Segundo Nivel**

Esta propiedad contiene la denominación o descripción *abreviada* del Segundo Nivel, (abreviatura que debería estar en consonancia con el idioma utilizado en la definición del primer nivel de la estructura al que está asociado).

A modo de *ejemplo* y si el Idioma utilizado en la definición del Primer Nivel de la Estructura es el español:

| Claves del 1er. y 2º Nivel | Descripción     | Vernáculo      | Abreviatura  |
| :-----------:              | :-----------    | :----------    | :------      | 
| ESP  - 001                 | Andalucía       | Andalucía      | AN           |
| ESP  - 002                 | Aragón          | Albacete       | AR           |
| ESP  - 009                 | Cataluña        | **Catalunya**  | CAT          |
| ...                        | ...             | ...            | ...          | 
## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que el Código del Segundo Nivel de la Estructura está inhabilitado para poder ser empleado en la configuración de los catálogos del Sistema.

### **Nivel Real**

Esta propiedad establece que el Código del Segundo Nivel de la Estructura Geográfica es un Nivel Real o un Nivel Genérico (puede existir un único Registro con esta Propiedad sin activar por cada Primer Nivel de la estructura)

`NOTA`: Esta propiedad es de uso interno, creada por y para uso del núcleo de la Aplicación.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Denominaciones Locales de los Niveles de la Estructura Geográfica](./DEFINICION-Denominacion-Nivel-Estructura-Geografica.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del Segundo Nivel de la Estructura Geográfica?

Una práctica que se recomienda como modelo es utilizar las codificaciones realizadas por el Servicio de Correos Local y cargarlas AS-IS en el Sistema.

## **Audiencia**

[Tabla TRON: A1000104]:<>