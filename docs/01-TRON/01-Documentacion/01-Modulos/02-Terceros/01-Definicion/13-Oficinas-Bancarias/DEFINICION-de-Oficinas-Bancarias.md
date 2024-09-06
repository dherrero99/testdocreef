![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de las Oficinas Bancarias {#definicion-de-las-oficinas-bancarias}

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar las Sucursales u Oficinas de las entidades Bancarias en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

- [Datos Identificativos](#datos-identificativos)
- [Datos de Contacto](#datos-de-contacto)
- [Propiedades Operativas](#propiedades-operativas)
- [Otras Propiedades](#otras-propiedades)

## Datos Identificativos

### **Compañía**

Este Atributo del catálogo de Sucursales bancarias contiene el código de la compañía sobre la que se está realizando la definición de la Oficina Bancaria.

### **Código de Actividad del Tercero**

Esta propiedad indicará el código de la Actividad del Tercero que se asocian a las Oficinas Bancarias puesto que en el Nuevo Modelo de Información de Terceros, las entidades bancarias y sus Sucursales se identifican en el sistema con una clave de actividad específica.

`NOTA`: Su valor es la constante **'41'** puesto que esta es una de las actividades que corresponden al núcleo y por ello no puede ser modificado.

### **Tipo Documento Identificador**

En el nuevo Modelo de Información de Terceros y por coherencia con la información del del resto de Personas Físicas o Jurídicas las Oficinas bancarias se deben identificar en el sistema con un tipo de documento identificativo y una clave asociada.

El valor del tipo de documento identificativo es **THP** siempre y cuando no tengan asociados documentos identificativos.

### **Clave del Documento Identificador**

En el nuevo Modelo de Información de Terceros y por coherencia con los datos del resto de Terceros, las Sucursales u Oficinas bancarias se identifican en el sistema con un código de actividad propio además de un tipo de documento identificativo y una clave asociada.

Este atributo contendrá el código del Tipo de documento Identificador asociado a la Sucursal Bancaria

### **Código Entidad Bancaria**

Este atributo será __la clave__ del banco a la que estará asociada la sucursal bancaria que se esté definiendo.

### **Clave Oficina Bancaria**

Este atributo será __la clave__ por la que se va a identificar la sucursal bancaria que estará asociada al código de Entidad Bancaria previamente capturado.

A modo de ejemplo, y para el código AAAA que identifica al 'BANCO Santander' como su entidad Bancaria, la Clave '0001' sería la clave de la Sucursal Bancaria ubicada en C/Campos Elíseos, 35., la clave '0002' sería la clave de la sucursal bancaria ubicada en Avda. Dr. García Tapia,... etc.

### **Nombre Oficina**

Este atributo contiene el __nombre__ por el que se identifica a la Sucursal Bancaria en el Sistema. 

### **Abreviatura Oficina Bancaria**

Este atributo contiene el __nombre__ abreviado por el que se puede identificar a la Sucursal Bancaria X perteneciente al Banco Y en el Sistema. 

## Datos de Contacto

### **Primer Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **primer** nivel de la estructura con el que se va a identificar geográficamente a la Sucursal Bancaria.

### **Segundo Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **segundo** nivel de la estructura con el que se va a identificar geográficamente a la Sucursal Bancaria.

### **Tercer Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **tercer** nivel de la estructura con el que se va a identificar geográficamente a la Sucursal Bancaria.

### **Cuarto Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **cuarto** nivel de la estructura con el que se va a identificar geográficamente a la Sucursal Bancaria..

### **Nombre del Cuarto Nivel de la Estructura Geográfica**

Este atributo contiene la descripción que corresponde al cuarto nivel de la estructura geográfica si bien y puesto que no en todos los países se cuenta con este nivel de detalle, puede contener información complementaria.

### **Cuarto Nivel Vernáculo de la Estructura Geográfica**

Este atributo contiene la clave del **cuarto** nivel de la estructura con la que se va a identificar geográficamente y en idioma vernáculo a las Oficinas Bancarias.

### **Nombre vernáculo del Cuarto Nivel de la Estructura Geográfica**

El propósito de este atributo es contener la nomenclatura del cuarto nivel de la estructura geográfica, en donde estará ubicada la Sucursal Bancaria, en lengua vernácula.

### **Tipo de Domicilio**

Este atributo ha de contener la *tipología* del Domicilio de la sucursal bancaria de acuerdo con el *uso y explotación* que posteriormente quiera realizar localmente la aseguradora con esta información.

A modo de **ejemplo** sus valores podrían ser:

- Calle.
- Avenida.
- Cerrada.
- Carretera.
- Paseo.
- ...

`NOTA`: Es necesario que el Departamento de Tecnología Local identifique sus valores en los catálogos del Sistema que identifican las *Listas de Valores* puesto que los valores prefijados por el núcleo pueden no ser aquellos de uso común en el país, teniendo en mente además que los valores serán de __uso transversal__ en la aplicación y no de uso específico para la configuración de las oficinas bancarias.

### **Domicilio**

Estos Atributos contienen la descripción del domicilio de acuerdo con la ubicación geográfica y tipología del domicilio de la Sucursal Bancaria además de permitir la captura de información complementaria que facilite la ubicación de esta.

### **Código Postal**

Este atributo contiene la clave del Código Postal en donde está ubicada la Oficina Bancaria.

### **Apartado Postal**

Este atributo contiene la clave del Apartado Postal perteneciente a la Oficina Bancaria, normalmente ubicado en una oficina de Correos, que le permite recibir correspondencia y paquetes sin tener que entregar su dirección física concreta. 

### **Dirección Correo Electrónico**

Este atributo contiene la dirección de correo electrónico corporativo de la Sucursal Bancaria.

### **Prefijo Telefónico del País**

Este atributo contiene el Prefijo del País Telefónico correspondiente al número telefónico de la Sucursal Bancaria.

A modo de ejemplo, en España el prefijo es +34, en México +52 y en Argentina +54.

### **Prefijo Zonal Telefónico**

Este atributo contiene el Prefijo Zonal Telefónico que corresponde al número telefónico de la Oficina Bancaria.

A modo de ejemplo, 

- En España el prefijo zonal de Madrid es el 91, el de Barcelona 93, ...
- En México la Clave Lada local que corresponde a Monterrey, Nuevo León es 81, la de Ciudad de México es 55,...

### **Número Fax**

Este atributo contiene el Número Telefónico del Fax correspondiente a la Oficina Bancaria.

### **Número Telefónico**

Este atributo contiene el Número Telefónico que corresponde al Teléfono de la Sucursal Bancaria.

### **Extensión Telefónica**

Caso de ser necesario, este atributo contendrá la Extensión Telefónica correspondiente al Teléfono de atención de la Oficina Bancaria.

## Propiedades Operativas

### **Código Interno Sucursal**

Este atributo contiene el código interno de la Oficina Bancaria de acuerdo con la configuración de la estructura Territorial **propia** de la entidad Bancaria.

### **Clave SWIFT**

Este atributo contiene el código SWIFT (acrónimo de Society for Worldwide Interbank Financial Telecommunication), también denominado código BIC (Bank Identifier Code), que no es sino una serie alfanumérica de 8 u 11 dígitos que se utiliza para identificar al banco receptor de una transferencia internacional.

¿Cuándo se aplica el código SWIFT / BIC?

El código SWIFT / BIC se aplica únicamente en aquellos países que no pertenecen a la Zona SEPA (o Zona única de Pagos en Europa) comprendida por los 28 países de la Unión Europea, además de Liechtenstein, Islandia, Noruega, Andorra, Mónaco, San Marino, Suiza, Reino Unido y Ciudad del Vaticano Estado.

`NOTA`: Los tres últimos dígitos son opcionales y en caso de aparecer hacen referencia a la sucursal en la que se encuentra la cuenta en concreto. Si no estuvieran presentes se entiende que pertenece a la oficina central del banco y por tanto el código SWIFT sería el configurado a nivel de la Entidad Bancaria.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad indica en el Sistema que la Sucursal Bancaria está inhabilitada para poder ser utilizada y asociada en las operaciones de captura y/o modificación de Terceros Físicos y/o Jurídicos.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)
- [Entidades Bancarias](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/12-Entidades-Bancarias/DEFINICION-de-Entidades-Bancarias.md#titulo)
- [Estructura Geográfica](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/03-Estructura-geografica/DEFINICION-Estructura-Geografica.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna aclaración operativa que deba ser tomada en consideración en el uso y definición de la tabla de Entidades Bancarias del Sistema?
