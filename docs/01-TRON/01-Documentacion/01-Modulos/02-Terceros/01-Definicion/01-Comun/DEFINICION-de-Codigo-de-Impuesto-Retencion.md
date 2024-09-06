![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (Ramón: Colocar el enlace al documento de definición de los impuestos y retenciones de la Tesorería A1001100)

# DEFINICIÓN de Impuestos y Retenciones por Actividad {#titulo}

## Contexto

Las entidades Aseguradoras están obligadas a retener o ingresar a cuenta cuando satisfagan o abonen rentas sujetas a retención o ingreso a cuenta, por los rendimientos derivados de actividades profesionales o por tratarse de rentas sujetas a retención en los términos establecidos en los Artículos del Impuesto de la Renta de las personas físicas o Jurídicas y de acuerdo a la Legislación Local.
 
Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de identificar y asociar a las Actividades de los Terceros 0, 1 o n posibles Códigos de Impuestos o Retenciones en un catálogo de información que se entrega a las entidades inicialmente vacío de contenido.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la asociación del impuesto o Retención a la actividad del Tercero.

### **Código de Actividad del Tercero**

Esta propiedad indica en el sistema el código de la Actividad del Tercero como por ejemplo Asegurados, Agentes, Clínicas, Peritos, ... 

### **Código del Impuesto / Retención del Tercero**

Esta propiedad indica en el sistema el código del Impuesto o Retención asociado a la actividad del Tercero. Como *ejemplo* y para la actividad 1 - Asegurados:

| Impuesto / Retención      |  Significado      |
| -----------               | -----------       |
| EXE                       | Tercero Exento    |
| R10                       | Retención 10%     |
| R15                       | Retención 15%     |
| IVA                       | IVA               |
| ...                       | ...               |

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)
- [Códigos de Impuestos y Retenciones - Tesorería](../../../../../../01-TRON/NOLINK.md)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición del Catálogo de Impuestos y Retenciones de Terceros en el Sistema?

La responsabilidad en la nomenclatura y definición de los códigos de retención e impuestos corresponde a la **Dirección de Administración y Finanzas** de la entidad MAPFRE local.

[Tabla TRON: A1001341]:<>