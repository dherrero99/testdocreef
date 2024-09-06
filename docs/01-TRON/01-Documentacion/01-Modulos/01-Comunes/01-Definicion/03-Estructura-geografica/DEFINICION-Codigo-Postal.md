![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Códigos Postales {#titulo}

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar los Códigos Postales asociados a la estructura Geográfica en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

### **Código del Primer Nivel**

Este atributo contiene la clave que identificará el Primer Nivel de la estructura Geográfica.

### **Código del Segundo Nivel**

Este atributo contiene la clave que identificará el Segundo Nivel de la estructura Geográfica.

### **Código del Tercer Nivel**

Este atributo contiene la clave que identificará el Tercer Nivel de la estructura Geográfica.

### **Código del Cuarto Nivel**

Este atributo contiene la clave que identificará el Cuarto Nivel de la estructura Geográfica.

### **Código del Quinto Nivel**

Este atributo sostiene la clave que identifica al Quinto Nivel de la estructura Geográfica.

### **Código Postal**

Esta Propiedad contiene la clave que identifica el Código Postal asociado a los cinco niveles de la estructura geográfica.

A modo de *ejemplo* y si el Idioma utilizado en la definición del Primer Nivel de la Estructura es el español para ESP - España / 13 - Madrid y 28 - Madrid:

| Claves de Niveles 1/2/3/4 | Clave/Nombre 5º Nivel          | Código Postal    |
| :-----------:             | :-----------                   | :----------      |
| ESP - 13 - 28 - 0001      | ZZZZ - Todas las Calles        |  28607           |
| ...                       | ...                            | ...              |
| ESP - 13 - 28 - 0002      | ZZZZ - Todos los Distritos     |  **28801**       |
| ESP - 13 - 28 - 0002      | **ZZZZ** - Todos los Distritos |  **28802**       |
| ESP - 13 - 28 - 0002      | **0001** - Barriada 1          |  **28803**       |
| ...                       | ...                            | ...              |
| ESP - 13 - 28 - 0003      | ZZZZ - Todos los Distritos     | *28100*          |
| ESP - 13 - 28 - 0003      | ZZZZ - Todos los Distritos     | *28108*          |
| ...                       | ...                            | ...              |
| ESP - 13 - 28 - 0004      | **0A0B** - No aplica           | *28921*          |
| ...                       | ...                            | ...              |

`NOTA`: Información obtenida de [Correos](https://www.correos.es/es/es/herramientas/codigos-postales/detalle)

### **Descripción del Código Postal**

Esta propiedad contiene la denominación o descripción del Código Postal (denominación que por coherencia debería estar en consonancia con el idioma utilizado en la definición del primer nivel de la estructura al que está asociado).

### **Descripción Vernácula del Cuarto Nivel**

Esta propiedad contiene la denominación o descripción del Cuarto Nivel de la Estructura Geográfica de acuerdo con el idioma vernáculo del Primer Nivel de la estructura geográfica al que pertenezca.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que el Código Postal está inhabilitado para poder ser empleado en la configuración de los catálogos de la Estructura Geográfica.

### **Nivel Real**

Esta propiedad establece que el Código Postal es un Código Real o un Nivel Genérico (puede existir un único Registro con esta Propiedad sin activar por cada subconjunto conformado por el Primer, Tercer y Cuarto Niveles de la estructura Geográfica)

`NOTA`: Esta propiedad es de uso interno, creada por y para uso del núcleo de la Aplicación.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Denominaciones Locales de los Niveles de la Estructura Geográfica](./DEFINICION-Denominacion-Nivel-Estructura-Geografica.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de los Códigos Postales de la Estructura Geográfica?

Una práctica que se recomienda como modelo es cargar y mantener en el tiempo las codificaciones realizadas por el Servicio de Correos Local.

## **Audiencia**

[Tabla TRON: A1000103]:<>