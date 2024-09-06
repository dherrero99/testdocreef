![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN del Segundo Nivel de la Estructura de Canales {#titulo}

## Contexto

Las *Agrupaciones* son conjuntos de [Fuentes de Producción](./DEFINICION-Nivel3-Fuente-de-Producccion.md) conformados por los [tipos de Clientes Distribuidores](./DEFINICION-Nivel1-Cliente-Distribuidor.md), sus [canales de comercialización] y otros Atributos adicionales que determinan características relevantes tales como su Vinculación (si son exclusivos, vinculados o multi compañía), de Ubicación (si el contacto se realiza en un punto de venta, en una oficina MAPFRE de atención al público o en una Oficina MAPFRE sin atención al público), Oferta de Productos (Multi producto, Especializado, Mono producto) y Canal de Origen del Cliente.

Corporativamente se han determinado una serie Agrupaciones principales por las cuales se debe informar desde las entidades MAPFRE y su configuración se realiza en el **segundo nivel** de la estructura de canales.

- [Propiedades Generales](#propiedades-generales)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía para la que se está definiendo el Cliente Distribuidor en el sistema.

### **Código del Primer Nivel**

Este atributo identifica la clave que identificará al Primer Nivel de la estructura de canales en el Sistema:

- Directo.
- Red Propia.
- Red Externa.
- Bancario.
- Acuerdos.

### **Código del Segundo Nivel**

Este atributo identifica la clave que identificará al Segundo Nivel de la estructura de canales en el Sistema.

### **Descripción del Segundo Nivel**

Esta propiedad contiene la denominación o descripción de la clave del Primer Nivel de la estructura de Canales.

### **Abreviatura del Segundo Nivel**

Este Atributo contiene la denominación o descripción de la clave del Primer Nivel de la estructura de Canales en formato abreviado.

La codificación y nomenclatura de la estructura quedaría como:

| Clave del Segundo Nivel | Descripción              | Abreviatura  |
| :-----------:           | :-----------             | :------      |
| 10                      | Oficinas Directas        | OFD.         |
| 11                      | Directo Grandes Cuentas  | DGC.         |
| 12                      | Directo Digital          | DD.          |
| 13                      | Directo Telefónico       | DT.          |
| 24                      | Delegados                | DEL.         |
| 25                      | Agentes Exclusivos       | AG.EX.       |
| 36                      | Agentes Vinculados       | AG.V.        |
| 37                      | Agentes No Vinculados    | AGNV.        |
| 38                      | Corredores Locales       | CORL.        |
| 39                      | Corredores Globales      | CORG.        |
| 410                     | Bancario                 | BANC.        |
| 511                     | Acuerdos                 | ACU.         |

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que la Agrupación del Cliente Distribuidor está inhabilitada para poder ser utilizada en su asignación a los Agentes o Intermediarios de la Entidad.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

1. ¿Existe alguna premisa que deba ser tomada en consideración localmente en la codificación, uso y definición del catálogo de Agrupaciones en el Sistema?

    No es posible alterar la codificación mínimamente preestablecida en el sistema para este Nivel de la Estructura de Canales.

## Audiencia

  - negocio
  - analista
  - implementador
  - desarrollador

[canales de comercialización]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos-Comunes.md#canal-canal>

[Tabla TRON: A1000722]:<>