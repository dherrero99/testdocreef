![Imagen LOGO](./00-Imagen/logo-TRON.png) width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Cuarto Nivel de la Estructura Geográfica {#titulo}

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar los Cuartos niveles de la estructura Geográfica en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

### **Código del Primer Nivel**

Este atributo contiene la clave que identificará al Primer Nivel de la estructura Geográfica.

### **Código del Tercer Nivel**

Este atributo identifica específicamente la clave que identificará al Tercer Nivel de la estructura Geográfica.

### **Código del Cuarto Nivel**

Este atributo identifica específicamente la clave que identificará al Cuarto Nivel de la estructura Geográfica que estará asociada en el catálogo a la clave del Tercer nivel de la estructura y que estará a su vez asociada en el catálogo a la clave del primer nivel de la estructura.

A modo de *ejemplo* y si el Idioma utilizado en la definición del Primer Nivel de la Estructura es el español para ESP - España / 28 - Madrid:

| Clave  de Niveles 1/3  | Clave del Cuarto Nivel  | Descripción       |
| :-----------:          | :-----------            | :----------       |
| ESP - 28               | 0001                    | Álamo, EL         |
| ESP - 28               | 0002                    | Alcalá de Henares |
| ESP - 28               | 0003                    | Alcobendas        |
| ESP - 28               | 0004                    | Alcorcón          |
| ...                    | ...                     | ...               |

### **Descripción del Cuarto Nivel**

Esta propiedad contiene la denominación o descripción del Cuarto Nivel (denominación que debería estar en coherencia con el idioma utilizado en la definición del primer nivel de la estructura al que está asociado).

### **Descripción Vernácula del Cuarto Nivel**

Esta propiedad contiene la denominación o descripción del Cuarto Nivel de la Estructura Geográfica (descripción que debería estar en consonancia con el idioma utilizado en la configuración del primer nivel de la estructura geográfica con el que está conectado).

### **Abreviatura del Cuarto Nivel**

Esta propiedad contiene la denominación o descripción *abreviada* del Cuarto Nivel (al igual que con el Atributo anterior, debería estar en consonancia con el idioma utilizado en la definición del primer nivel de la estructura al que está asociado)

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que el Código del Cuarto Nivel de la Estructura está inhabilitado para poder ser empleado en la configuración de los catálogos de la Estructura Geográfica definida en el Sistema.

### **Nivel Real**

Esta propiedad establece que el Código del Cuarto Nivel de la Estructura Geográfica es un Nivel Real o un Nivel Genérico (puede existir un único Registro con esta Propiedad sin activar por cada subconjunto de Primer/Tercer y Cuarto Nivel de la estructura)

`NOTA`: Esta propiedad es de uso interno, creada por y para uso del núcleo de la Aplicación.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Denominaciones Locales de los Niveles de la Estructura Geográfica](./DEFINICION-Denominacion-Nivel-Estructura-Geografica.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del Cuarto Nivel de la Estructura Geográfica?

Una práctica que se recomienda como modelo es utilizar las codificaciones realizadas por el Servicio de Correos Local y cargarlas AS-IS en el Sistema.

## **Audiencia**

[Tabla TRON: A1000102]:<>