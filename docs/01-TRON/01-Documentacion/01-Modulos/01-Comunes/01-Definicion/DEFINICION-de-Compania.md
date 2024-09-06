![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (Revisión de enlaces, lenguaje, detalle de atributos como descripción, teléfonos, direcciones,...)

# DEFINICIÓN de las Compañías/Entidades del Sistema {#titulo}

## Objetivo

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de codificar múltiples compañías en un repositorio de información específico que se entrega inicialmente a las instalaciones *parcialmente* vacío de contenido.

El sistema permite definir y codificar hasta un máximo de **99** diferentes entidades pudiendo denominar e identificar individualmente cada una de ellas mediante una denominación o texto descriptivo además de una abreviatura y un nombre corto.

En la definición de una compañía, las Propiedades y funcionalidades existentes en el sistema se agrupan en:

-   [Propiedades Generales](#propiedades-generales)
-   [Propiedades Operativas de Terceros](#propiedades-operativas-de-terceros)
-   [Propiedades Operativas Financieras y Comerciales](#propiedades-operativas-financieras-y-comerciales)
-   [Propiedades Operativas de Emisión](#propiedades-operativas-de-emisión)
-   [Propiedades Operativas de Siniestros](#propiedades-operativas-de-siniestros)
-   [Resto Propiedades Operativas](#resto-propiedades-operativas)
-   [Otras Propiedades de las Entidades](#otras-propiedades)

## Propiedades Generales

### **Clave y Código de Identificación**

Estos dos atributos del catálogo de compañías indicarán la manera de identificación tributaria utilizada localmente en cada unos de los países.

Por ejemplo: El Número de Identificación Fiscal o **NIF** es la manera de identificación tributaria utilizada en España para:

-   Las personas físicas con documento nacional de identidad **DNI** o
    con número de identificación de extranjero **NIE** asignados por el
    Ministerio del Interior.

-   Las personas jurídicas, cuyo antecedente fue el **CIF**.

### **Clave de Identificación Patronal**

Este atributo sirve para identificar en el catálogo de compañías la clave de identificación patronal de acuerdo con la legislación del país en el que se ubica la compañía.

### **Clave de Identificación Societaria**

Este atributo sirve para identificar en el catálogo de compañías la clave de identificación contable de acuerdo con las directrices Corporativas de MAPFRE.

`NOTA:` Debe corresponder con el identificador de la sociedad en el sistema Contable Corporativo: **0002** (Mapfre España), **0233** (Mapfre Paraguay Seguros), **0378** (Mapfre Dominicana, S.A.), ...

### **Razón Social**

Este Atributo del catálogo de compañías indicará el nombre con que la entidad o sociedad mercantil MAPFRE está registrada local y legalmente.

### **Estructura Geográfica**

Una vez definida la Estructura Geográfica que va a usarse en la entidad se debe actualizar el catálogo de entidades y asignar la estructura correspondiente a la Razón Social.

### **Dirección y Apartado Postal**

Varios Atributos del Catálogo de definición permiten codificar e identificar la dirección postal de la Sede Social de la entidad y su apartado postal.

### **Teléfono y Fax**

Varios Atributos del Catálogo de definición permiten identificar el prefijo telefónico del País, la clave del área y el teléfono de la entidad así como su número de Fax.

`NOTA:` No es necesario en todos los países definir una clave de área para efectuar las conexiones telefónicas.

### **Nombre y Apellidos del CEO**

Estos dos atributos del catálogo de compañías indicarán el Nombre y Apellidos del máximo Responsable de la compañía.

### **Moneda del País**

Este atributo del catálogo de definición de las entidades, identifica en el sistema el código **ISO** de moneda del país.

### **Compañía Reaseguro Externo**

Este atributo del catálogo de definición de las entidades, identifica en el sistema el código de la entidad en el sistema de Reaseguro ***RE21.***

### **Festivos Laborables**

Existen dos atributos en la Tabla de configuración del catálogo de entidades que permiten identificar si los sábados y domingos son o no días festivos.

### **Actividad que identifica la entidad**

Este atributo del catálogo de definición de las entidades, identifica el código de actividad que identificará la entidad en el sistema.

`NOTA:` Este dato tiene un valor constante de **'39'**

## Propiedades Operativas de Terceros

### **Tratamiento y Pospuesto**

Estos dos atributos le indican al sistema si se va a permitir o no, en los programas que actualizan la información de los terceros, capturar el Tratamiento y/o el Pospuesto en aquellas intervenciones identificadas como **personas físicas**

A modo de ejemplo, la activación de ambas marcas permitirían...

- Ingresar como prefijos: \[Ilustrísimo /Ilmo. - Excelentísimo/Excmo. - Doña - Sr. - Sra. - Srta. ,... \]
- Ingresar como sufijos \[ Junior / Jr. - Senior / Sr. - II - Segundo -, ...\]

### **Captura Apellidos en Personas Físicas**

Existen dos atributos en el catálogo de definición de entidades que modulan el comportamiento de los programas que actualizan la información de los terceros, forzando o no la captura del primer y del segundo apellido en aquellas intervenciones identificadas como **personas físicas**

### **Nombre Compuesto**

Este atributo del catálogo de entidades modula el comportamiento de los programas que actualizan la información de los terceros, permitiendo la captura del nombre en dos campos separados cuando el nombre de la persona Física es un nombre compuesto.

### **Muestra Segundo Apellido**

Este atributo del catálogo de entidades modula el comportamiento de los programas de captura de los datos de los Terceros, mostrando y permitiendo o no la captura del segundo Apellido siempre y cuando la información corresponda a una Persona Física.

En Estados Unidos de Norteamérica, por ejemplo, no suele ser común indicar un segundo apellido como en los países latinos.

`NOTA:` Este dato debe estar en consonancia con el atributo que obliga o no a la captura del segundo apellido.

### **R.G.P.D. & Herramienta R.G.P.D**

Este atributo del catálogo de entidades le indica al sistema si aplica o no el Reglamento General de Protección de Datos para personas físicas tanto en el tratamiento y gestión de sus datos personales como en su libre circulación.

Caso que esté activado se debe indicar el nombre de la Herramienta de Protección de Datos utilizada por la compañía como por ejemplo ... 'Sin herramienta Externa', 'OneTrust', 'Ley Orgánica de Protección de Datos Europea, 'Agencia Española de Protección de Datos', ...

`NOTA:` Es Responsabilidad del departamento de Tecnología y Procesos de la Entidad MAPFRE local codificar adecuadamente en el sistema los posibles valores de las Herramientas.

### **Captura del Código Postal o de la Dirección Postal**

Este atributo del catálogo de entidades modula el comportamiento de los programas que actualizan la información de los terceros haciendo que el orden de la captura se efectúe:

- **Primero** el Código Postal, y a partir del mismo se rellenan automáticamente los datos de la Dirección Postal.
- **Primero** la Dirección Postal, y a partir de su información se obtiene el Código Postal.

### **Extensión Postal**

Este atributo del catálogo de entidades habilita o no en los programas que actualizan la información de los terceros la captura de la extensión del Código Postal.

### **Terceros Duplicados Inter compañías**

Este atributo en el catálogo modula el comportamiento del sistema haciendo que el programa de Captura y Modificación de Usuarios automáticamente replique o no la información del Tercero en todas y cada una de las entidades definidas en el sistema.

### **Identificación de Terceros Duplicados**

Este atributo en el catálogo de definición de compañías hace que el programa de Captura y Modificación de Terceros ejecute o no automática e internamente la tarea de comprobar si el Tercero ya existe en el sistema con otro Tipo y Clave de Documento identificativo al objeto de evitar, en la medida de lo posible, información de Terceros duplicados.

### **ID único de Terceros**

Este atributo en el catálogo de definición de compañías hace que el programa de Captura y Modificación de Terceros asigne o no automáticamente una clave única y de uso interno en la información del Tercero Capturado.

`NOTA:` Caso que este atributo esté activado, el departamento de Tecnología y Procesos tendrá que implementar y desarrollar un *componente* *software* que se encargue de realizar la codificación y asignación de la clave única de acuerdo a los criterios que determinen y consideren adecuado las Direcciones de Negocio de la entidad MAPFRE local.

## Propiedades Operativas Financieras y Comerciales

### **Empleados de Intermediarios**

Este atributo del catálogo de entidades habilita o no la funcionalidad del núcleo existente para la identificación de los empleados de los Agentes Intermediarios de las pólizas.

### **Formato de Cuenta Corriente**

Este atributo del catálogo de entidades le indica al sistema el formato de la cuenta corriente en la captura de información bancaria de la persona Física o Jurídica.

### **Tipo de I.V.A**

Este atributo del catálogo le indica al sistema si se ha de contemplar o no la captura del Tipo de IVA en el alta y modificación de los Terceros siendo sus posibles valores: Exento, Normal o Reducido.

`NOTA:` Este dato tiene tiene afectación en las Liquidaciones del proceso de Gestión de Siniestros y Prestaciones.

## Propiedades Operativas de Emisión

### **Actividad por Defecto**

Este atributo permite indicar el código de la actividad por defecto en el que se basará la captura de la información de otros Terceros (siempre y cuando estos últimos se correspondan con tipologías de Terceros con Código de Actividad 1: Conductores, Asegurados, Beneficiarios,...).

### **Longitud de los Textos Anexos y Clausulas**

Existen dos atributos en el catálogo de definición de entidades que limitan la longitud de las líneas de texto en los textos anexos y en las clausulas en el Programa de Emisión.

### **Límite de Primas** {#limite-de-primas}

Para el Control en la Prevención del Lavado de Dinero existen tres atributos del catálogo de entidades que permiten al sistema limitar el importe de las primas emitidas y en vigor tanto para **personas físicas** como para **personas jurídicas**, en ambos casos expresadas en la misma **moneda**.

Los límites aplican no sólo al Tomador sino a cualquiera de las figuras intervinientes en la Póliza tal y como posibles Beneficiarios, Asegurados, Pagadores, Tomadores Alternos, ...

`NOTA:` Es responsabilidad de la Entidad definir e implementar los procedimientos de actuación a efectos de gestionar y explotar adecuadamente la información.

### **Reservadas**

En el caso de los Ramos Técnicos de Caución & Crédito, este atributo en el catálogo de definición de las entidades, modula el comportamiento del sistema controlando y validando en su caso que tanto los textos anexos como las cláusulas de las pólizas de estos Ramos Técnicos no tengan palabras/sentencias reservadas.

`NOTA:` Es responsabilidad de la Entidad definir en un catálogo específico las palabras o frases que se quieran controlar expresamente.

## Propiedades Operativas de Siniestros

### **Programa Apertura Siniestros**

Este atributo del catálogo de definición de las entidades, identifica el código del Programa con el que se va a realizar la apertura de siniestros.

### **Programa Apertura de Expedientes**

Este atributo del catálogo de definición de las entidades, identifica el código del Programa con el que se va a realizar la apertura de expedientes en el sistema.

`NOTA:` Es responsabilidad del departamento de Tecnología y Procesos de la Entidad MAPFRE local indicar la nomenclatura de ambos programas.

### **Oficina en Control Técnico de Siniestros**

Este atributo del catálogo de definición de las entidades, identifica el código de la estructura comercial de la compañía que se ha de tomar en consideración para la ejecución de los controles técnicos en el proceso de gestión de siniestros y prestaciones: o bien la Oficina **Emisora** o bien la Oficina **Tramitadora**.

### **Captura Número de Siniestro en Registro de Facturas**

Este atributo del catálogo de definición de las entidades, modula el comportamiento del sistema forzando la captura o no del número de Siniestro en el Programa de Registro de Facturas del módulo de Siniestros del núcleo.

## Resto Propiedades Operativas

### **Información Parcial**

Este atributo en el catálogo de definición de las entidades, modula el comportamiento del sistema afectando a los Programas de Consulta de Información para mostrar o no parcialmente la información del Tercero.

### **Identificación Usuarios**

Este atributo en el catálogo de definición de las entidades, modula el comportamiento del sistema afectando los Programas de Alta y Modificación de Usuarios para forzar a que la identificación de los Usuarios del sistema obligue o no a capturar tanto el Tipo de documento como la Clave del Documento.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Por qué existen dos abreviaturas en la definición de la entidad?

El ámbito en el uso de estos dos campos es puramente local no existiendo ninguna obligación a nivel corporativo para su utilización. Por ejemplo y en el caso de MAPFRE Filipinas en una de estas abreviaturas podría identificarse el tipo de entidad empresarial de MAPFRE Insular colocando el Corp. en uno de ambos atributos, ...

[Tabla TRON: A1000900]:<>