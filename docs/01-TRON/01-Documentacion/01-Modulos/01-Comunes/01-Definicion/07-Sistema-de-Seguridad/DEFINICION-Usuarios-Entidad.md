![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Usuarios de la Entidad {#titulo}

## Contexto

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar la relación de Usuarios de la entidad MAPFRE en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

- [Datos Identificativos](#datos-identificativos)
- [Datos de Contacto](#datos-de-contacto)
- [Propiedades Operativas](#propiedades-operativas)

## Datos Identificativos

### **Compañía**

Este Atributo del catálogo de Usuarios por Entidad contiene el código de la compañía sobre la cual se está realizando la definición de los Usuarios.

### **Clave de Usuario**

Este Atributo del catálogo de Usuarios de la Entidad contiene el código del Usuario, denominado 'NUUMA' en MAPFRE.

### **Nombre de Usuario**

Este Atributo del catálogo de Usuarios de la Entidad contiene el nombre y los apellidos del Usuario.

### **Número de Usuario**

Este Atributo del catálogo de Usuarios de la Entidad contiene el código numérico único del Usuario.

### **Tipo Documento Identificador**

En el Modelo de Información de Terceros y por coherencia con la información del del resto de Personas Físicas o Jurídicas los Usuarios se deben identificar en el sistema con un tipo de documento identificativo y una clave asociada.

Este atributo contendrá el Tipo de documento Identificador de acuerdo con la configuración realizada en la tabla específica del sistema.

### **Clave del Documento Identificador**

En el Modelo de Información de Terceros y por coherencia con la información del del resto de Personas Físicas o Jurídicas los Usuarios se deben identificar en el sistema con un tipo de documento identificativo y una clave asociada.

Este atributo contendrá la clave única del Tipo de documento Identificador.

## Datos de Contacto

### **Dirección Correo Electrónico**

Este atributo contiene la dirección de correo electrónico corporativo del primer nivel de la estructura comercial.

## Propiedades Operativas

### **Clave del Tercer Nivel**

Este atributo contiene el __código__ del Tercer Nivel de la Estructura Comercial en el cual el Usuario se ubica físicamente.

### **Agrupamiento de Usuarios**

Este atributo contiene el __código__ del Agrupamiento de Usuarios al que pertenece el Usuario, código que permite a la entidad clasificar internamente al colectivo de Usuarios.

### **Información Parcial**

Este atributo identifica si el Usuario, en aquellos programas que realizan Consultas sobre la información del sistema y así lo establecen funcionalmente, puede o no visualizar la información detalladamente o solamente puede consultar los datos de manera agregada.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Documentos Identificadores](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Documento-Identificativo.md#titulo)
- [Tercer Nivel de la Estructura Comercial](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/02-Estructura-Comercial/DEFINICION-Nivel3-Estructura-Comercial.md#titulo)

## Preguntas frecuentes

1. ¿Existe alguna recomendación que pueda ser tomada en consideración en el uso y definición del Catálogo de Usuarios de la Entidad?

    Es una buena práctica codificar a los usuarios en este catálogo de la misma manera con la que se identifica a los usuarios en el **directorio activo** de la Entidad.

[Tabla TRON: G1002700]:<>