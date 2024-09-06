![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Quinto Nivel de la Estructura Geográfica {#titulo} 

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar los Quintos niveles de la estructura Geográfica en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

### **Código del Primer Nivel**

Este atributo contiene la clave que identificará al Primer Nivel de la estructura Geográfica.

### **Código del Segundo Nivel**

Este atributo identifica específicamente la clave que identificará al Segundo Nivel de la estructura Geográfica.

### **Código del Tercer Nivel**

Este atributo identifica específicamente la clave que identificará al Tercer Nivel de la estructura Geográfica.

### **Código del Cuarto Nivel**

Este atributo identifica específicamente la clave que identificará al Cuarto Nivel de la estructura Geográfica.

### **Código del Quinto Nivel**

Este atributo identifica específicamente la clave que identificará al Quinto Nivel de la estructura Geográfica que estará asociada en el catálogo a las claves de los niveles de la estructura geográfica.

A modo de *ejemplo* y si el Idioma utilizado en la definición del Primer Nivel de la Estructura es el español, para el país España - ESP, La Comunidad de Madrid - 13, la Provincia de Madrid - 28 y La Ciudad de Madrid - 0001:

| Claves Niveles 1/2/3/4   | Clave del Quinto Nivel  | Descripción     |
| :-----------:            | :-----------            | :----------     |
| ESP - 13 - 28  - 0001    | AAA1                    | Arganzuela      |
| ESP - 13 - 28  - 0001    | AAA2                    | Barajas         |
| ESP - 13 - 28  - 0001    | AAA3                    | Carabanchel     |
| ESP - 13 - 28  - 0001    | AAA4                    | Centro          |
| ...                      | ...                     | ...             |

### **Idioma**

Esta propiedad identifica el Idioma empleado en la definición del Nivel de la estructura, como por ejemplo con los códigos que identifiquen a los idiomas español, inglés, turco,...

### **Descripción del Quinto Nivel**

Esta propiedad contiene la denominación o descripción del Quinto Nivel, denominación que debería estar en coherencia con el idioma utilizado en la definición al que está asociado.

### **Nivel Real**

Esta propiedad establece que el Código del Quinto Nivel de la Estructura Geográfica es un Nivel Real o un Nivel Genérico (puede existir un único Registro con esta Propiedad sin activar a igualdad en los cuatro niveles de la estructura.

NOTA: Esta propiedad es de uso interno, creada por y para uso del núcleo de la Aplicación.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que el Código del Quinto Nivel de la Estructura está inhabilitado para poder ser empleado en la configuración de los catálogos del Sistema.

### **Fecha de Validez**

Esta propiedad le indica al Sistema la fecha a partir de la cual la clave del quinto nivel de la estructura está plenamente operativa en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los niveles.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Denominaciones Locales de los Niveles de la Estructura Geográfica](./DEFINICION-Denominacion-Nivel-Estructura-Geografica.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del Quinto Nivel de la Estructura Geográfica?

Una práctica que se recomienda como modelo es utilizar las codificaciones realizadas por el Servicio de Correos Local y cargarlas AS-IS en el Sistema.

## **Audiencia**

[Tabla TRON: DF_GRS_NWT_XX_ZNF_SBD]:<>