![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Tercer Nivel de la Estructura de Canales {#titulo}

## Contexto

Una *Fuente de Producción* es una clave que identifica unívocamente en el sistema el [tipo de Cliente Distribuidor](./DEFINICION-Nivel1-Cliente-Distribuidor.md), el [canal de comercialización] y los Atributos adicionales (de vinculación, ubicación, oferta de productos y canal de origen del cliente) que la constituyen.

![Fuente de Producción](./00-Imagen/Fuente-de-Produccion.png)

La Configuración de las Fuentes de Producción se realiza en el **tercer nivel** de la estructura de canales.

- [Propiedades Generales](#propiedades-generales)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo la clave de la Fuente de Producción en el sistema.

### **Código del Primer Nivel**

Este atributo identifica la clave que identificará al Primer Nivel de la estructura de canales o **Tipos de Clientes Distribuidores** en el Sistema:

- Directo.
- Red Propia.
- Red Externa.
- Bancario.
- Acuerdos.

### **Código del Segundo Nivel**

Este atributo identifica la clave que identificará al Segundo Nivel de la estructura de canales o **Agrupaciones** en el Sistema:

- Oficinas Directas.
- Directo Grandes Cuentas.
- Directo Digital.
- Directo Telefónico.
- Delegados.
- Agentes Exclusivos.
- Agentes Vinculados.
- Agentes No Vinculados.
- Corredores Locales.
- Corredores Globales.
- Bancario.
- Acuerdos.

### **Código del Tercer Nivel**

Este atributo identificará la clave del Tercer Nivel de la estructura de canales o **Fuentes de Producción** en el Sistema:

### **Descripción del Tercer Nivel**

Esta propiedad contiene la denominación o descripción de la clave del Tercer Nivel de la estructura de Canales o Fuente de Producción del Cliente Distribuidor.

### **Abreviatura del Tercer Nivel**

Este Atributo contiene la denominación o descripción de la clave del Tercer Nivel de la estructura de Canales en formato abreviado.

De manera ilustrativa y no exhaustiva, la codificación y nomenclatura de las Fuentes de Producción en el sistema para un Cliente Distribuidor de tipo **'Directo'**, un canal de venta **'Telefónico'** y una vinculación **'Exclusiva'**, atendiendo a su ubicación y oferta de productos podría quedar como:

| Clave del Tercer Nivel  | Descripción                                              |
| :-----------:           | :-----------                                             |
| 1001                    | Producción Telefónica - Oficina Directa - Multi Producto |
| 1002                    | Producción Telefónica - Oficina Directa - Específica     |
| 1003                    | Contact Center Propio                                    |
| 1004                    | Contact Center Propio Exclusivo                          |
| 1005                    | Contact Center Propio                                    |
| 1006                    | Contact Center Propio Exclusivo                          |

En cambio, la codificación y nomenclatura de las Fuentes de Producción en el sistema para un Cliente Distribuidor de tipo **'Red Propia'**, un canal de venta **'Presencial'** y una vinculación **'Exclusiva'**, atendiendo a su ubicación y oferta de productos podría quedar como:

| Clave del Tercer Nivel  | Descripción                 |
| :-----------:           | :-----------                |
| 2401                    | Delegado MAPFRE             |
| 2402                    | Delegado Específico MAPFRE  |
| 2501                    | Agente Exclusivo            |
| 2502                    | Agente Exclusivo Específico |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que la Fuente de Producción del Cliente Distribuidor está inhabilitada para poder ser utilizada en su asignación a los Agentes o Intermediarios de la Entidad.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Relación de Agentes y Fuentes de Producción](./DEFINICION-Relacion-Fuente-de-Produccion-Agente.md)

## Preguntas frecuentes

1. ¿Existe alguna premisa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Fuentes de Producción en el Sistema?

    En las entidades MAPFRE recae la __responsabilidad__ de analizar y determinar la granularidad de sus Fuentes de Producción de acuerdo con las necesidades operativas locales pero sin perder de vista que tienen que estar sincronizadas con las clasificaciones corporativas de **Agrupaciones y Clientes Distribuidores**.

## Audiencia

  - negocio
  - analista
  - implementador
  - desarrollador

[Canal de comercialización]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos-Comunes.md#canal-canal>

[Tabla TRON: A1000723]:<>