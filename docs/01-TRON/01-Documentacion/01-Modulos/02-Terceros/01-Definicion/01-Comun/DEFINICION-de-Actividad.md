![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de las Actividades de los Terceros {#titulo}

## Contexto

Las actividades que los Terceros Físicos o Jurídicos tienen asociadas identifican inequívocamente los procesos, procedimientos y flujos operativos en el sistema en los que intervienen o pueden intervenir, e.g:

Si capturamos en el sistema la información de una persona física y la identificamos en el sistema con la actividad asociada a un Intermediario o Agente, este código de actividad le permitirá entrar de manera automática en el proceso de devengo de comisiones de la entidad MAPFRE, proceso por el que percibirá una retribución económica consistente, entre otros conceptos, de una parte proporcional de las primas conseguidas en su labor comercial directa o a través de su intervención o colaboración. 

En cambio si a la misma persona la hubiéramos identificado en el sistema como un Perito o como un Empleado, por lo que tendría asignados códigos diferentes de actividad al código de actividad de Intermediario del ejemplo anterior, esta persona podría respectivamente estar involucrada en tareas específicas de asignación y peritaje dentro del proceso de Gestión de Siniestros y Prestaciones o beneficiarse automáticamente de un descuento comercial en la contratación de sus pólizas en el proceso de Emisión.

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y codificar las diferentes Actividades de los Terceros, sean estos personas Físicas o Jurídicas, en un catálogo de información específico que se entrega a las entidades **con contenido**:

`IMPORTANTE:` Los códigos de actividad del 1 al 99 (además del código 999) están **reservados** y son de uso exclusivo por el núcleo del sistema.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición de la Actividad del Tercero.

### **Código de Actividad del Tercero**

Esta propiedad indica en el sistema el código de la Actividad del Tercero. 

En idioma español la relación de Actividades que provee el núcleo es:

- ASEGURADOS
- AGENTE
- PERITOS
- INSPECTORES
- MEDICOS
- ABOGADOS
- PROCURADORES
- SUPERVISORES
- TRAMITADORES
- PROVEEDORES
- EJECUTIVOS DE CUENTA
- COBRADORES
- ASEGURADORAS
- REASEGURADORAS
- EMPLEADOS
- BROKERS
- TALLERES CONCERTADOS
- CLÍNICAS
- JUZGADOS
- CRISTALEROS
- CERRAJEROS
- PLOMEROS
- ELECTRICISTAS
- GRÚAS
- INVESTIGADORES
- RECUPERADORES
- AJUSTADORES
- HERREROS
- TRIBUNALES
- TERCEROS AUTOS
- TERCEROS PERSONAS
- TERCEROS PATRIMONIALES
- DEPÓSITOS (SALVAMENTOS)
- NOTARIAS
- CENTRO PERITACIÓN
- COMISARIAS
- EMPLEADOS DE AGENTES
- FILIAL
- COMPAÑÍA
- ENTIDADES BANCARIAS
- OFICINAS BANCARIAS
- NIVEL1 EST.COMERCIAL
- NIVEL2 EST.COMERCIAL
- NIVEL3 EST.COMERCIAL
- REPRESENTANTES
- OTROS BENEFICIARIOS

### **Descripción de la Actividad del Tercero**

Esta propiedad le indica al sistema cual es la denominación o descripción de la Actividad del Tercero.

## Propiedades Operativas

### **La Actividad Permite Documentos Ficticios**

Esta propiedad le indica al sistema si el código de la actividad permite o no asociarse a Terceros identificados con tipos de documentos definidos como documentos no reales o ficticios.

### **¿La Actividad corresponde a un Proveedor?**

Este atributo le indica al sistema si la Actividad asociada a un Tercero va a identificar o no a los Proveedores en el sistema.

Por ejemplo, los siguientes códigos de Actividad tienen habilitada esta propiedad:

| Código de Actividad       |  Descripción            |
| -----------               | -----------             |
| 17                        | Talleres Concertados    |
| 20                        | Cristaleros             |
| 21                        | Cerrajeros              |
| ...                       | ...                     |

### **Código de Tercero**

Esta propiedad le indica al Sistema si la información del Tercero asociado a la actividad contempla o no la existencia y generación de un código interno del Tercero.

### **Generación Automática**

Siempre y cuando el atributo del código del tercero esté activado el sistema permite definir si el código interno se va o no a generar automáticamente.

### **Código de Estructura**

Esta propiedad le indica al sistema el Código de la *Estructura* o *Programa* del Sistema que permite realizar la captura, el mantenimiento y la consulta de la información de los Terceros que tengan asociado el código de actividad.

### **Agrupación de Estructuras**

Este atributo le indica al sistema la agrupación de estructuras a la que pertenece el Código de la estructura de mantenimiento.

`NOTA:` Es responsabilidad de la Dirección de Tecnología local la definición e identificación del nombre de la estructura y de la agrupación de estructuras que se vayan a asignar a la Actividad del Tercero.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Estructuras](../../../../NOLINK.md)
- [Documentos Identificativos](./DEFINICION-de-Documento-Identificativo.md#titulo)

## Preguntas frecuentes

(1) ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación y uso de las Actividades de Terceros en el Sistema?

No existe Corporativamente una preferencia o recomendación para establecer o estandarizar en el sistema la codificación de las actividades de los Terceros, excepto por **respetar obligatoriamente** los códigos de actividades propios del núcleo de la aplicación.

[Tabla TRON: A1002200]:<>