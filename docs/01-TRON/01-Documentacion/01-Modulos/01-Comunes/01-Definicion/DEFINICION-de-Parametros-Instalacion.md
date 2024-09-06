![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==En construcción==

# DEFINICIÓN de Los Parámetros Iniciales de la Instalación {#titulo}

El núcleo del Sistema permite identificar y codificar los Parámetros que intervienen y modulan el comportamiento y funcionalidad de los distintos módulos que lo componen, en un catálogo de información que se entrega a las entidades inicialmente con contenido *parcial*.

En el catálogo se configuran los diferentes parámetros de acuerdo con las siguientes agrupaciones:

- [Parámetros **Transversales**](#propiedades-transversales)
- [Parámetros Gestión de **Pólizas y Contratos**](#propiedades-operativas-emisión)
- [Parámetros Gestión de **Siniestros y Prestaciones**](#propiedades-operativas-siniestros)
- [Parámetros Gestión de **Personas Físicas y/o Jurídicas**](#propiedades-operativas-de-terceros)
- [Parámetros del **Sistema**](#propiedades-del-sistema)
- [Otras Propiedades](#otras-propiedades)

`NOTA`: Es competencia de la Dirección de Tecnología Local la identificación y definición de todos estos parámetros.

## Propiedades Transversales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de Codificar y Clasificar los medios de Cobro y Pago de los Terceros en un catálogo de información específico que se entrega inicialmente a las instalaciones vacío de contenido.

## Propiedades Operativas Emisión

### **Hora/Minutos por defecto en Suplementos**

Este Atributo identifica, en aquellos Ramos que tengan configurada la obligatoriedad de su captura, la Hora y minutos que se mostrarán como *parte* de la Fecha de Efecto de la póliza o del suplemento en el Proceso de Emisión.

A modo de ejemplo:

- 00:00
- 12:00 

### **BPM en Proceso de Gestión de Pólizas y Contratos**

Este Atributo identifica si el proceso de Gestión de Pólizas y Contratos tiene o no activada su ejecución vía Business Process Management (BPM).

## Propiedades Operativas Siniestros

### **BPM en Proceso de Gestión de Siniestros y Prestaciones**

Este Atributo identifica si el proceso de Gestión de Siniestros y Prestaciones tiene o no activada su ejecución vía Business Process Management (BPM).

## Propiedades Operativas de Terceros

### **El Sistema emplea el nuevo Modelo de Terceros**

El modelo de datos de Terceros se ha evolucionado, para por un lado cumplir el Modelo de Referencia de Clientes establecido en MAPFREa nivel corporativo y por otro para dotarle de mayor funcionalidad y flexibilidad. 

Es por ello por lo que se han definido este parámetro para distinguir e indicar si los países están utilizando o no el nuevo modelo de datos de Terceros.

IMPORTANTE: Los [buzones](../../../../../01-TRON/99-Terminos/TRON-Terminos.md#buzon) utilizados en los Procesos Masivos de Terceros sirven para **ambos modelos: el nuevo y el antiguo** pero es necesario tener instalados los esquemas NewTron si se utiliza el modelo antiguo.

### **Tipo Documento Identificador Terceros**

Siempre y cuando las nuevas Actividades de Terceros creadas en el núcleo como consecuencia de la evolución del Nuevo Modelo de Datos de Terceros no tuvieran asociadas ningún tipo de documentos identificadores, este atributo identificará el *Tipo de Documento Identificador* que en la captura **inicial** de una persona física o jurídica perteneciente a estas actividades el sistema asignará por defecto.

### **Código Identificador Terceros**

Como consecuencia de la evolución del Nuevo Modelo de Datos de Terceros y de las nuevas Actividades de Terceros creadas, es necesario identificar cual es el código genérico de los Terceros para realizar determinados accesos a la Base de Datos de la Aplicación.

### **Cuentas Bancarias Múltiples**

Siempre y cuando la instalación utilice el Modelo de Datos de Terceros antiguo, la activación de este parámetro modula la funcionalidad del sistema permitiendo la posibilidad de capturar múltiples cuentas bancarias o solamente una (a diferencia de si la instalación emplea el Nuevo Modelo de Datos en el que se permite **indistintamente** la captura de 1 o n cuentas bancarias).

### **Tarjetas Múltiples**

Siempre y cuando la instalación utilice el Modelo de Datos de Terceros antiguo, la activación de este parámetro modula la funcionalidad del sistema permitiendo la posibilidad de capturar múltiples Tarjetas o solamente una (a diferencia de si la instalación emplea el Nuevo Modelo de Datos en el que se permite **indistintamente** la captura de 1 o n Tarjetas).

## Propiedades del Sistema

### **Base de Datos del Sistema**

Este Atributo del Catálogo identifica si la Base de Datos que soporta la información del Sistema es o no ORACLE.

### **Conjunto de Caracteres del Sistema**

Un conjunto de caracteres es un sistema de codificación para que las computadoras sepan cómo reconocer un carácter, incluidas letras, números, signos de puntuación y espacios en blanco.

Este Atributo del Catálogo identifica el Código del Conjunto de Caracteres, alfabéticos o no, que cuentan con unas características comunes en su estructura y en su estilo y que se emplean en la aplicación, como por ejemplo el Código 'iso-8859-1'

### **Clave de la Instalación**

Este Atributo identifica localmente la instalación o país en el que se ejecuta la aplicación, permitiendo distinguir en ciertos catálogos de la aplicación si los registros que contienen pertenecen al núcleo o son extensiones del mismo particularizadas por la Entidad.

A modo de ejemplo:

- La Clave 'TRN' corresponde al código de instalación del Núcleo, 
- La Clave 'MMT' corresponde a la instalación de MAPFRE MiddleSea (Malta), 
- La Clave 'EUR' sería la instalación de MAPFRE Chile (EuroAmérica Seguros originalmente)
- ...

### **Número Máximo de Registros en Consultas**

Este Atributo del Catálogo identifica el número máximo de registros que se pueden obtener en una consulta a la Base de Datos de la Aplicación minimizando así el impacto global de la consulta sobre el rendimiento del sistema.

### **Número Máximo de Registros en Consultas del Generador de Productos**

Este Atributo del Catálogo identifica el número máximo de registros que se pueden obtener en una consulta específicamente sobre los Catálogos del Generador de Productos minimizando así el impacto global de la consulta sobre el rendimiento del sistema.

### **Idioma de la Instalación**

Este Atributo identifica el idioma por defecto con el que se mostrarán las etiquetas en el conjunto de Programas de la Aplicación. 

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Idioma de la Instalación](./DEFINICION-de-Idioma.md#titulo)

## Preguntas frecuentes

**(1)** ¿Son excluyentes los dos Modelos de Información de Terceros en una instalación?

Sí, o bien se utiliza el Modelo Antiguo o bien se emplea el Nuevo Modelo.

---
"BGN_DAY_WEK";                          "1";"DIA EN QUE EMPIEZA LA SEMANA"
"CPB_VAL";                              "S";"COMPATIBLE"
"ETD_ACV_QRY";                          "N";"CONSULTA ACTIVIDAD EXTENDIDA"
"FORMATO_FECHA_SIN_SEPARADOR";          "DDMMYYYY";"FORMATO FECHA LIMPIO"
"FRM_DAT_HOR";                          "HH"; "FORMATO HORA 24"
"FRM_DAT_MNH";                          "MM";"FORMATO MES DE UNA FECHA"
"FRM_DAT_SCN";                          "SSSSS";"FORMATO SEGUNDOS DE UNA FECHA"
"FRM_DAT_TME_WIT_SPR";                  "DDMMYYYYHH24MISS";"FORMATO FECHA-HORA DE UNA FECHA"
"FRM_DAT_TME_WIT_SPR_FE";               "ddMMyyyyHHmmss";"FORMATO FECHA-HORA DE UNA FECHA PARA FE"
"FRM_DAT_WIT_SPR_FE";                   "ddMMyyyy";"FORMATO FECHA LIMPIO PARA FE"
"FRM_DAT_WTH_SPR_FE";                   "dd/MM/yyyy";"FORMATO PARA CAMPOS DE FECHA PARA FE. VALOR POR DEFECTO DD/MM/YYYY"
"FRM_DAT_YER";                          "YYYY";"FORMATO AÑO DE UNA FECHA"
"FRM_DAT_YER_FE";                       "yyyy";"FORMATO AÑO DE UNA FECHA PARA FE"
"FRM_SHR_DAT_WIT_SPR";                  "MMYY";"FORMATO FECHA CORTO"
"FRM_SHR_DAT_WIT_SPR_FE";               "MMyy";"FORMATO FECHA CORTO PARA FE"
"FRM_SHR_DAT_YER";"YY";                 "FORMATO CORTO AÑO DE UNA FECHA"
"FRM_SHR_DAT_YER_FE";                   "yy";"FORMATO CORTO AÑO DE UNA FECHA PARA FE"
"FRM_TME_EDT";                          "HH24:MI:SS";"FORMATO HORA EDITADO DE UNA FECHA"
"FRM_TME_WIT_SPR";                      "HHmmss";"FORMATO HORA DE UNA FECHA"

"MCA_COBROS_MULTICIA";                  "N";"INDICA SI SE PERMITE REALIZAR EL COBRO DE RECIBOS DE VARIAS CIAS CON UNA UNICA CAJA"
"MCA_CTR_ACCESO_OP_TW_NWT";             "N";"INDICA SI UNA INSTALACION CONTEMPLA EL USO DE CONTROL ACCESO USUARIO A OPERACIONES NEWTRON"
"MCA_FEC_ACTU_EXTEND";                  "S";"INDICA SI SE DESEA LA FEC_ACTU TRUNCADA O EN FORMATO HH:MI:SS"
"MCA_MDT_THP_NEW";v                     "S";"DETERMINA SI SE UTILIZA O NO EL NUEVO MODELO DE DATOS DE TERCEROS"
"MCA_MOD_BANK_OFFICE";                  "N";"PARÁMETRO QUE INDICA SI SE PUEDE MODIFICAR EL ID. OFFICE DE LA CUENTA CUANDO EL TIPO DE CUENTA ES 2 (ABA NUMBER)"

"MCA_PARTITION_TABLE";                  "S";"DETERMINA SI LA APLICACION ESTA EN UNA VERSION IGUAL O SUPERIOR A ORACLE 9i"
"MCA_ROL_MENUOPCIONES";                 "N";"INDICA SI SE DESEA FILTRAR LOS MENUS DE OPCIONES POR ROL"
"MCA_SIEMPRE_A1000802";                 "N";"RECUPERAR DATOS LOCALES TERCEROS"

"NBR_MXM_RSK_RNS";                      "50";"NUMERO MAXIMO DE RIESGOS A TRATAR EN CADA LLAMADA  A SERVICIO GRABAR PROPUESTA DE  RE21"
"NO";"N";"NO"
"QRY_LTD_INY";                          "N";"CONSULTA ASEGURADO LIMITADA"
"SAV_TMP";                              "N";"GRABA TEMPORAL"

"TIP_FORMATO_LISTADO";                  "3";"TIPO DE FORMATO A USAR EN LOS LISTADOS (1 - LISTADO TEXTO, 2 - LISTADO EN CRISTAL REPORTS, 3 - LISTADO EN JASPER)"
"TXT_FORMATO_FECHA";                    "DD/MM/YYYY";"FORMATO PARA CAMPOS DE FECHA. VALOR POR DEFECTO DD/MM/YYYY"
"TXT_FORMATO_MMYYYY";                   "MMYYYY";"Formato para campos de fecha sin el dia. Valor por defecto MM-YYYY"
"TXT_MSPOOL_DIR";"/mnt/ap_tronweb_pre/lis";"DIRECTORIO ESTANDAR PARA LISTADOS DE MSPOOL (UTL_FILE) DEBE COINCIDIR CON EL ESPECIFICADOR EN ORACLE (INT.ORA) COMO DIRECTORIO QUE UTILIZA UTL_FILE."
"TXT_MSPOOL_DIR_REAL";                  "/mnt/ap_tronweb_pre/lis";"DIRECTORIO ESTANDAR PARA LISTADOS DE MSPOOL (UTL_FILE) DIRECTORIO DE EQUIPO SERVIDOR DE PROGRAMAS (PUEDE SER DIFERENTE AL EQUIPO SERVIDOR DE BASE DE DATOS)."
"TXT_SEPARADOR_DECIMALES";              ",";"FORMATO PARA SEPARADOR DE DECIMALES EN CAMPOS NUMERICOS."
"TXT_SEPARADOR_MILES";                  ".";"FORMATO PARA SEPARADOR DE MILES EN CAMPOS NUMERICOS."
"TXT_SQL_DIR";                          "/mnt/ap_tronweb_pre/sql";"DIRECTORIO ESTANDAR PARA ARCHIVOS SQL GENERADOS (UTL_FILE) DEBE COINCIDIR CON EL ESPECIFICADOR EN ORACLE (INT.ORA) COMO DIRECTORIO QUE UTILIZA UTL_FILE."
"TXT_SQL_DIR_REAL";                     "/mnt/ap_tronweb_pre/sql";"DIRECTORIO ESTANDAR PARA ARCHIVOS SQL GENERADOS (UTL_FILE) DIRECTORIO DE EQUIPO SERVIDOR DE PROGRAMAS (PUEDE SER DIFERENTE AL EQUIPO SERVIDOR DE BASE DE DATOS)."
"URL_APPLICATION_SERVER";               "http://10.76.142.46:8080/twserver/mapfre.srv.SVTronWeb";"URL DL SERVIDOR DE APLICACIONES"

"YES";"S";"SI"

[Tabla TRON: G0000000]:<>