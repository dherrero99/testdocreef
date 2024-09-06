![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Entidades Bancarias {#titulo}

La banca o el sistema bancario, es el conjunto de entidades o instituciones que, dentro de una economía determinada, prestan servicios financieros. Entre los bancos, existen algunos tipos, como los bancos de inversión, que a diferencia de los bancos comerciales se centran en ciertos tipos de servicios financieros y de consultoría.

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar múltiples entidades Bancarias en un repositorio de información específico que se entrega inicialmente a las instalaciones *vacío* de contenido.

- [Datos Identificativos](#datos-identificativos)
- [Datos de Contacto](#datos-de-contacto)
- [Propiedades Operativas](#propiedades-operativas)
- [Otras Propiedades](#otras-propiedades)

## Datos Identificativos

### **Compañía**

Este Atributo del catálogo de entidades bancarias contiene el código de la compañía sobre la que se está realizando la definición de la Entidad Bancaria.

### **Código de Actividad del Tercero**

Esta propiedad indicará el código de la Actividad del Tercero que se asocian a las entidades Bancarias puesto que en el Nuevo Modelo de Información de Terceros, las entidades bancarias se identifican en el sistema con una clave de actividad específica.

`NOTA`: Su valor es la constante **'40'** puesto que esta es una de las actividades que corresponden al núcleo y por ello no puede ser modificado.

### **Tipo Documento Identificador**

En el nuevo Modelo de Información de Terceros y por coherencia con la información del del resto de Personas Físicas o Jurídicas las entidades bancarias se deben identificar en el sistema con un tipo de documento identificativo y una clave asociada.

El valor del tipo de documento identificativo es **THP** siempre y cuando no tengan asociados documentos identificativos propios.

### **Clave del Documento Identificador**

En el nuevo Modelo de Información de Terceros y por coherencia con los datos del resto de Terceros, las entidades bancarias se identifican en el sistema con un código de actividad propio además de un tipo de documento identificativo y una clave asociada.

Este atributo contendrá el código del Tipo de documento Identificador.

A modo de ejemplo, el Banco de Santander se identifica en el Reino de España con el Tipo de Documento **NIF** cuya clave es **A-39000013**

### **Clave Entidad Bancaria**

Este atributo será __la clave__ por la que se va a identificar los distintos bancos que operan localmente con la entidad MAPFRE.

### **Nombre Entidad Bancaria**

Este atributo contiene el __nombre__ por el que se identifica a la Entidad Bancaria en el Sistema. 

### **Abreviatura Entidad Bancaria**

Este atributo contiene el __nombre__ abreviado por el que se puede identificar a la Entidad Bancaria en el Sistema. 

## Datos de Contacto

### **Primer Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **primer** nivel de la estructura con la que se va a identificar geográficamente a las Entidades Bancarias que operan localmente con la entidad MAPFRE.

### **Segundo Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **segundo** nivel de la estructura con la que se va a identificar geográficamente a las Entidades Bancarias que operan localmente con la entidad MAPFRE.

### **Tercer Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **tercer** nivel de la estructura con la que se va a identificar geográficamente a las Entidades Bancarias que operan localmente con la entidad MAPFRE.

### **Cuarto Nivel de la Estructura Geográfica**

Este atributo contiene la clave del **cuarto** nivel de la estructura con la que se va a identificar geográficamente a las Entidades Bancarias que operan localmente con la entidad MAPFRE.

### **Nombre del Cuarto Nivel de la Estructura Geográfica**

Este atributo contiene información que corresponde al cuarto nivel de la estructura geográfica si bien y puesto que no en todos los países se cuenta con este nivel de detalle, puede contener información complementaria.

### **Cuarto Nivel Vernáculo de la Estructura Geográfica**

Este atributo contiene la clave del **cuarto** nivel de la estructura con la que se va a identificar geográficamente a las Entidades Bancarias que operan localmente con la entidad MAPFRE, si bien a la manera propia del lugar o país de nacimiento de uno.

### **Nombre vernáculo del Cuarto Nivel de la Estructura Geográfica**

El propósito de este atributo es contener la nomenclatura del cuarto nivel de la estructura geográfica en lengua vernácula.

### **Tipo de Domicilio**

Este atributo ha de contener la *tipología* del Domicilio la entidad bancaria de acuerdo con el *uso y explotación* que posteriormente quiera realizar localmente la aseguradora con esta información.

A modo de **ejemplo** sus valores podrían ser:

- Calle.
- Avenida.
- Cerrada.
- Carretera.
- Paseo.
- ...

NOTA: Es necesario que el Departamento de Tecnología Local identifique sus valores en los catálogos del Sistema que identifican las *Listas de Valores* puesto que los valores prefijados por el núcleo pueden no ser aquellos de uso común en el país, teniendo en mente además que los valores serán de __uso transversal__ en la aplicación y no de uso específico para la configuración de las entidades bancarias.

### **Domicilio**

Estos Atributos contienen la descripción del domicilio de acuerdo con la ubicación geográfica y tipología del domicilio de la entidad bancaria además de permitir la captura de información complementaria que facilite la ubicación de la entidad bancaria.

### **Código Postal**

Este atributo contiene la clave del Código Postal en donde está ubicada la entidad Bancaria.

### **Apartado Postal**

Este atributo contiene la clave del Apartado Postal perteneciente a la entidad Bancaria, normalmente ubicado en una oficina de Correos, que le permite recibir correspondencia y paquetes sin tener que entregar una dirección física concreta. 

### **Dirección Correo Electrónico**

Este atributo contiene la dirección de correo electrónico corporativo de la entidad Bancaria.

### **Prefijo Telefónico del País**

Este atributo contiene el Prefijo del País Telefónico correspondiente al número telefónico Corporativo de la entidad Bancaria.

A modo de ejemplo, en España el prefijo es +34, en México +52 y en Argentina +54.

### **Prefijo Zonal Telefónico**

Este atributo contiene el Prefijo Zonal Telefónico que corresponde al número telefónico Corporativo de la entidad Bancaria.

A modo de ejemplo, 

- En España el prefijo zonal de Madrid es el 91, el de Barcelona 93, ...
- En México la Clave Lada local que corresponde a Monterrey, Nuevo León es 81, la de Ciudad de México es 55,...

### **Número Fax**

Este atributo contiene el Número Telefónico del Fax Corporativo de la entidad Bancaria.

### **Número Telefónico**

Este atributo contiene el Número Telefónico que corresponde al Teléfono Corporativo de la entidad Bancaria.

### **Extensión Telefónica**

Caso de ser necesario, este atributo contendrá la Extensión Telefónica correspondiente al Teléfono Corporativo de la entidad Bancaria.

## Propiedades Operativas

### **Tipo de Entidad**

Este atributo ha de contener la *tipología* de la entidad bancaria de acuerdo con el *uso y explotación* que posteriormente quiera realizar localmente la aseguradora con esta información.

A modo de **ejemplo** sus valores podrían ser:

- Bancos, cajas de ahorros y cooperativas de crédito.
- Entidades de dinero electrónico.
- Entidades de pago.
- Establecimientos financieros de crédito.
- Establecimientos de venta y compra de moneda extranjera.
- Sucursales de entidades extranjeras.
- Intermediación financiera en el mercado de crédito. 
- ...

`NOTA`: Es necesario que el Departamento de Tecnología Local identifique sus valores en los catálogos del Sistema que identifican las *Listas de Valores* puesto que no existen valores prefijados por el núcleo.

### **Tipo de Institución Bancaria**

Este atributo permite contener una *tipología o clasificación bancaria* de acuerdo con el *uso y explotación* que posteriormente quiera realizar localmente la aseguradora con esta información.

A modo de **ejemplo**, si la entidad local quisiera explotar la información de sus clientes para conocer de manera agregada con qué bancos operan estos, sus valores podrían ser:

- Bancos minoristas. 
- Bancos comerciales. 
- Bancos de desarrollo comunitario. 
- Bancos de inversión. 
- Bancos en línea o neobancos. 
- Cooperativas de crédito. 
- Asociaciones de ahorro y préstamo.

### **Tipo de Empresa Jurídica**

Este atributo contiene el tipo de empresa jurídica de la entidad bancaria.

### **Tipo de Domiciliación Bancaria**

Este atributo contiene la *tipología* del proceso de Domiciliación bancaria que la entidad MAPFRE local contempla con la entidad bancaria y de acuerdo con el acuerdo comercial pactado entre ambas partes.

Sus valores son:

- Domiciliación con cuentas bancarias.
- Domiciliación con Tarjetas.
- Domiciliación indistintamente con Tarjetas y/o Cuentas Bancarias.

### **Fecha de Constitución**

Este atributo contiene la fecha en la que se constituyó legalmente la entidad bancaria en el país en el que está operando.

### **Clave SWIFT**

Este atributo contiene el código SWIFT (acrónimo de Society for Worldwide Interbank Financial Telecommunication), también denominado código BIC (Bank Identifier Code), que no es sino una serie alfanumérica de 8 u 11 dígitos que se utiliza para identificar al banco receptor de una transferencia internacional.

¿Cuándo se aplica el código SWIFT / BIC?

El código SWIFT / BIC se aplica únicamente en aquellos países que no pertenecen a la Zona SEPA (o Zona única de Pagos en Europa) comprendida por los 28 países de la Unión Europea, además de Liechtenstein, Islandia, Noruega, Andorra, Mónaco, San Marino, Suiza, Reino Unido y Ciudad del Vaticano Estado.

### **Nacionalidad**

Este atributo contiene la clave del **primer nivel** de la estructura geográfica que corresponde al país de procedencia de la entidad bancaria.

### **Código de Referencia**

Este atributo contiene la clave de referencia de la entidad bancaria.

### **Código de Entidad Nueva**

Este atributo contiene el código de la entidad bancaria compradora en el supuesto que haya existido un proceso de concentración bancario y una entidad haya absorbido una u otras entidades bancarias.

### **Número de Días Extra**

Este atributo contiene el número de días que la entidad bancaria contempla para conformar la 'FECHA VALOR' en sus operaciones financieras.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad indica en el Sistema que la Entidad Bancaria está inhabilitada para poder ser utilizada y asociada en las operaciones de captura y/o modificación de Terceros Físicos y/o Jurídicos.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)
- [Documentos Identificadores](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Documento-Identificativo.md)
- [Estructura Geográfica](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/03-Estructura-geografica/DEFINICION-Estructura-Geografica.md#titulo)
- [Configuración de los Parámetros Iniciales](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/DEFINICION-de-Parametros-Instalacion.md#definición-de-los-parámetros-iniciales-de-la-instalación-titulo)

## Preguntas frecuentes

1. ¿Existe alguna aclaración operativa que deba ser tomada en consideración en el uso y definición de la tabla de Entidades Bancarias del Sistema?

    Siempre y cuando la actividad 40 asignada a las entidades bancarias no tuviera asociada ningún tipo de documento identificador, el valor que el sistema asignará en el atributo del *Tipo de Documento Identificativo en la captura **inicial** de una entidad bancaria será aquel que se define en la configuración de los parámetros de la instalación.