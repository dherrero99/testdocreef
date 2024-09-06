![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de los Medios de Cobro o Pago {#titulo}

- [Propiedades Generales](#propiedades-generales)
- [Propiedades Operativas](#propiedades-operativas)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de Codificar y Clasificar los medios de Cobro y Pago de los Terceros en un catálogo de información específico que se entrega inicialmente a las instalaciones vacío de contenido.

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición del Medio del Cobro o Pago.

### **Idioma**

Esta propiedad le indica al sistema el Idioma empleado en la definición como por ejemplo: español, inglés, turco, ...

### **Código del Medio de Cobro/Pago**

Esta propiedad indicará el código del Medio de Cobro/Pago que se está definiendo en el Sistema pudiendo definir para un mismo Tipo de Cobro/Pago distintos Códigos de Medios de Cobro/Pago.

### **Descripción del Cobro/Pago**

Esta propiedad indica la denominación o descripción de acuerdo con el idioma en el que se está definiendo el registro en el Sistema.

## Propiedades Operativas

### **Tipo del Medio de Cobro/Pago**

Este Atributo que está asociado al Código del Medio de Cobro/Pago, indica la Clasificación al que pertenece el Código del Medio de Cobro/Pago.

En idioma español la relación de Tipos que provee el núcleo es:

- Cuenta Bancaria.
- Tarjeta Bancaria.
- Pago Móvil/Celular.
- Monedero Virtual.
- Moneda Virtual.
- Pago On-line.

A modo de ejemplo, utilizando adecuadamente los Códigos y Tipos de Medios de Cobro o Pago...

| CÓDIGO MEDIO.       | TIPO MEDIO            | Descripción          |
| -----------         | -----------           | -------              |
| 001                 | Cuenta Bancaria       | Cuenta Corriente     |
| 002                 | Cuenta Bancaria       | Cuenta de Valores    |
| 003                 | Cuenta Bancaria       | Cuenta Plazos        |
| ...                 | ...                   | ...                  |
| AAA                 | Pago Móvil/Celular    | Apple Pay            |
| AAB                 | Pago Móvil/Celular    | Samsung Pay          |
| AAC                 | Pago Móvil/Celular    | Google Pay           |
| ...                 | ...                   | ...                  |
| AA1                 | Tarjeta Bancaria      | Visa                 |
| AA2                 | Tarjeta Bancaria      | Mastercard           |
| AA3                 | Tarjeta Bancaria      | American Express     |
| AA4                 | Tarjeta Bancaria      | Dinner's             |
| ...                 | ...                   | ...                  |

### **Tipo de Validación de los Medios de Cobro o Pago**

De acuerdo con el Tipo del Medio de Cobro/Pago del Tercero y por coherencia con las funcionalidades provistas en el núcleo del Sistema, este Atributo indicará el tipo de validación que se ha de ejecutar al introducir un valor en el programa de captura/mantenimiento del Tercero

En idioma español la relación de validaciones que se pueden efectuar es:

- Validación de Cuenta Bancaria.
- Validación de Teléfono.
- Validación de Tarjeta.
- Validación de Correo Electrónico.

### **Tipo de Enmascaramiento de los Medios de Cobro o Pago**

De acuerdo con el Tipo del Medio de Cobro/Pago del Tercero y por coherencia con las funcionalidades que provee el núcleo del Sistema, este Atributo indicará el tipo de enmascaramiento que se ha de ejecutar de acuerdo con el valor introducido en el programa de captura/mantenimiento del Tercero

En idioma español la relación de validaciones que se pueden efectuar es:

- Enmascaramiento de la Cuenta Bancaria.
- Enmascaramiento del Teléfono.
- Enmascaramiento de la Tarjeta.
- Enmascaramiento del Correo Electrónico.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad le indica al Sistema que el Medio de Cobro/Pago está inhabilitado para poder ser utilizado en las operaciones de captura y/o modificación del Tercero.

### **Fecha de Validez**

Esta propiedad le indica al Sistema la fecha a partir de la cual el Medio de Cobro o Pago está plenamente operativo en el sistema por lo que su correcto uso permite tener un histórico de los cambios efectuados en las definiciones de los medios.

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Actividades de Terceros](./DEFINICION-de-Actividad.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de los Códigos de Medios de Cobro/Pago de los Terceros en el Sistema?

Es `obligatorio` *respetar* los valores de los **Tipos del Medio de Cobro/Pago**, **Tipos de Validaciones** y **Tipos de Enmascaramientos** definidos y habilitados por el núcleo del Sistema.

[Tabla TRON: DF_THP_NWT_XX_PMD]:<>
[Tabla TRON: DF_THP_NWT_XX_ENT]:<>