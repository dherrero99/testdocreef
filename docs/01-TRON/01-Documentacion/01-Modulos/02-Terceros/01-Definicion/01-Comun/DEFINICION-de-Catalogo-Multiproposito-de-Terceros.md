![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Catálogo de Catálogos Multipropósito de Terceros {#titulo}

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la facilidad de definir y codificar datos de distinta naturaleza y condición en un Catálogo de Catálogos que se entrega inicialmente en las instalaciones vacío de contenido [(Pulsa aquí)](./DEFINICION-de-Catalogo-Multiproposito-de-Terceros.md#preguntas-frecuentes)

La definición de los códigos asociados de cada uno de los Catálogos de esta Tabla se realiza por compañía e idioma (Español , Inglés, ...) pudiendo denominar e identificar individualmente cada una de ellos mediante una denominación o texto descriptivo.

A modo de ejemplo, esta funcionalidad del sistema permite codificar conjuntamente los **Códigos de los Tipos de Sociedad** y los **Códigos de los Grupos Empresariales** que tienen que configurarse en el sistema para validar la información capturada en el proceso de Alta de las personas Jurídicas.

*Códigos de los Tipos de Sociedad*:

| Catálogo Sociedad Mercantil | Clave y Descripción         |
| -----------                 | -----------                 |
| 00001                       | Sociedad Anónima            | 
| 00002                       | Sociedad Limitada           |
| 00003                       | Sociedad Comanditaria       |
| ...                         | ...                         |

*Códigos de los Grupos Empresariales*:

| Catálogo Grupos Empresariales | Clave y Descripción       |
| -----------                   | -----------               |
| AAAA                          | Banco SANTANDER           | 
| BBBB                          | VOLKSWAGEN AG.            |
| CCCC                          | ABERTIS S.A.              |
| DDDD                          | GRUPO CARSO               |
| ...                           | ...                       |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema si el registro del Catálogo está inhabilitado para poder ser utilizada en las operaciones de captura y/o modificación del Tercero.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura es recomendada para complementar o evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes 

**(1)** ¿Cuales son los valores de los Catálogos que el núcleo del Sistema utiliza para reconocer sobre qué valores se han de realizar determinadas validaciones al capturar la información de un Tercero y por tanto **se deben respetar obligatoriamente**?

| Valores Catálogo | Descripción           |
| :-----------:    | :-----------          |
| 1                | Tipo de Sociedad      | 
| 2                | Grupo Empresarial     |
| 3                | Titulación            |
| 4                | Zonas Horarias        | 
| 5                | Segmentación Clientes |
| 6                | Dispositivo           |
| 7                | Canal                 | 

**(2)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del Catálogo de Catálogos en el Sistema?

No existe una preferencia ni recomendación para establecer o estandarizar en el sistema su codificación si bien la entidad MAPFRE debe analizar la conveniencia de utilizar transversalmente en los procesos de la compañía este catálogo de información para su correcta y posterior explotación.

[Tabla TRON: DF_THP_NWT_XX_CGT]:<>