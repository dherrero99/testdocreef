![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Primer Nivel de la Estructura Comercial {#titulo}

## Contexto

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar la estructura Comercial de la entidad MAPFRE en una estructura piramidal de **tres niveles** con repositorios de información específicos que se entregan inicialmente a las instalaciones *vacíos* de contenido.

## Objetivo

Conocer los atributos y características del Primer Nivel de la Estructura Comercial.

- [Datos Identificativos](#datos-identificativos)
- [Datos de Contacto](#datos-de-contacto)
- [Propiedades Operativas](#propiedades-operativas)
- [Otras Propiedades](#otras-propiedades)

## Datos Identificativos

### **Compañía**

Este Atributo del Primer Nivel de la Estructura Comercial contiene el código de la compañía sobre la que se está realizando su definición.

### **Código de Actividad del Tercero**

Esta propiedad indicará el código de la Actividad del Tercero que se asocian al primer nivel de la estructura comercial puesto que en el Nuevo Modelo de Información de Terceros, los niveles de la estructura se identifican en el sistema con una clave de actividad específica.

`NOTA`: Su valor es la constante **'42'** puesto que esta es una de las actividades que corresponden al núcleo y por ello no puede ser modificado.

### **Tipo Documento Identificador**

En el nuevo Modelo de Información de Terceros y por coherencia con la información del del resto de Personas Físicas o Jurídicas los niveles de la estructura comercial se deben identificar en el sistema con un tipo de documento identificativo y una clave asociada.

El valor del tipo de documento identificativo es **THP** siempre y cuando no tengan asociados documentos identificativos propios.

### **Clave del Documento Identificador**

En el nuevo Modelo de Información de Terceros y por coherencia con la información del del resto de Personas Físicas o Jurídicas los niveles de la estructura comercial se deben identificar en el sistema con un tipo de documento identificativo y una clave asociada.

Este atributo contendrá el código del Tipo de documento Identificador.

### **Clave del Primer Nivel**

Este atributo contiene el __código__ por el que se identificará el Primer Nivel de la Estructura Comercial en el Sistema.

### **Denominación del Primer Nivel**

Este atributo contiene el __nombre__ por el que se identifica al Primer Nivel de la Estructura Comercial en el Sistema.

### **Abreviatura del Primer Nivel**

Este atributo contiene el __nombre__ abreviado por el que se puede identificar al Primer Nivel de la Estructura Comercial.

## Datos de Contacto

### **Segundo Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **segundo** nivel de la Estructura Geográfica en la que está ubicado el primer nivel de la Estructura Comercial.

### **Tercer Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **tercer** nivel de la Estructura Geográfica en la que está ubicado el primer nivel de la Estructura Comercial.

### **Cuarto Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **cuarto** nivel de la Estructura Geográfica en la que está ubicado el primer nivel de la Estructura Comercial.

### **Nombre del Cuarto Nivel de la Estructura Geográfica**

Este atributo contiene información que corresponde al cuarto nivel de la estructura geográfica si bien y puesto que no en todos los países se cuenta con este nivel de detalle, puede contener información complementaria.

### **Tipo de Domicilio**

Este atributo ha de contener la *tipología* del Domicilio del primer nivel de la Estructura Comercial de acuerdo con la configuración, uso y explotación que posteriormente se quiera realizar localmente.

A modo de **ejemplo** sus valores podrían ser:

- Calle.
- Avenida.
- Cerrada.
- Carretera.
- Paseo.
- ...

`NOTA`: Es necesario que el Departamento de Tecnología Local identifique sus valores en los catálogos del Sistema que identifican las *Listas de Valores* puesto que los valores prefijados por el núcleo pueden no ser aquellos de uso común en el país, teniendo en mente además que los valores serán de __uso transversal__ en la aplicación y no de uso específico para la configuración del primer nivel de la estructura comercial.

### **Domicilio**

Estos Atributos contienen la información de detalle del domicilio del primer nivel de la estructura comercial de acuerdo con la ubicación geográfica y tipología del domicilio capturados.

### **Código Postal**

Este atributo contiene la clave del Código Postal en donde está ubicada el Domicilio del primer nivel de la estructura comercial.

### **Apartado Postal**

Este atributo contiene la clave del Apartado Postal perteneciente al primer nivel de la estructura comercial, normalmente ubicado en una oficina de Correos, que le permite recibir correspondencia y paquetes sin tener que entregar la dirección física concreta. 

### **Dirección Correo Electrónico**

Este atributo contiene la dirección de correo electrónico corporativo del primer nivel de la estructura comercial.

### **Nombre y Apellidos Responsable del nivel**

Estos atributos del repositorio de configuración contienen el nombre y los apellidos del responsable máximo del nivel de la estructura comercial definida.

### **Prefijo Telefónico del País**

Este atributo contiene el Prefijo del País Telefónico correspondiente al número telefónico Corporativo del nivel de la estructura comercial.

A modo de ejemplo, en España el prefijo es **+34,**g en México **+52** y en Argentina **+54**.

### **Prefijo Zonal Telefónico**

Este atributo contiene el Prefijo Zonal Telefónico que corresponde al número telefónico Corporativo del nivel de la estructura comercial.

A modo de ejemplo, 

- En España el prefijo zonal de Madrid es el **91**, el de Barcelona **93**, ...
- En México la Clave Lada local que corresponde a Monterrey, Nuevo León es **81**, la de Ciudad de México es **55**,...

### **Número Fax**

Este atributo contiene el Número Telefónico del Fax Corporativo del nivel de la estructura comercial.

### **Número Telefónico**

Este atributo contiene el Número Telefónico que corresponde al Teléfono Corporativo del nivel de la estructura comercial.

## Propiedades Operativas

### **Observaciones**

Este atributo puede contener información adicional/complementaria que se estime oportuno capturar en la configuración del **primer nivel** de la estructura comercial.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad indica en el Sistema que la clave del primer nivel de la estructura comercial está inhabilitada para ser utilizada en la captura y/o modificación de los niveles de la estructura comercial.

### **Emisión**

==Pendiente==

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)
- [Documentos Identificadores](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Documento-Identificativo.md#titulo)
- [Estructura Geográfica](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/03-Estructura-geografica/DEFINICION-Estructura-Geografica.md#titulo)

## Preguntas frecuentes

1. ¿Existe alguna aclaración operativa que deba ser tomada en consideración en la configuración, uso y definición de la tabla de primeros niveles de la estructura comercial en el sistema?

    Siempre y cuando la actividad 42 asignada al primer nivel de la estructura comercial no tuviera asociada ningún tipo de documento identificador, el valor que el sistema asignará en el atributo del *Tipo de Documento Identificador* será aquel que se define en la configuración realizada en los parámetros de la instalación.

2. ¿Se pueden solapar los usos de la Estructura Comercial y la Estructura de canales de Distribución?

    La Configuración de la Estructura de los Canales de distribución obedece a una **necesidad Corporativa concreta** para la obtención del *Margen de Contribución* por Cliente Distribuidor, mientras que la Configuración de la Organización Comercial obedece a funciones en las que se combinan factores de producción (capital, trabajo, recursos, tecnología, etc.) con actividades que maximizan el proceso de creación de valor de la entidad.

[Tabla TRON: A1000700]:<>