![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de la Relación de Agentes y Fuentes de Producción {#titulo}

## Contexto

Funcionalmente, el núcleo del Sistema cuenta con la posibilidad de configurar y asociar para cada uno de los Agentes de la Entidad las Fuentes de Producción **específicas** que cada uno de ellos puede utilizar.

- [Propiedades Generales](#propiedades-generales)
- [Otras Propiedades](#otras-propiedades)

## Propiedades Generales

### **Compañía**

Este atributo contiene el código de la compañía en la que se está asociando para una clave de agente determinada el código de la Fuente de Producción.

### **Agente**

Este atributo identifica la clave del Agente.

### **Código del Tercer Nivel**

Este atributo identificará la clave del Tercer Nivel de la estructura de canales o **Fuente de Producción** que se está asignando al agente.

## Otras Propiedades

### **Inhabilitación**

Esta propiedad establece que la Fuente de Producción del Cliente Distribuidor está inhabilitada para poder ser asignada en pólizas de nueva producción.

### **Fecha de Validez**

Esta propiedad establece la fecha a partir de la cual la asociación del Agente y la Fuente de Producción está disponible en el sistema para ser utilizada, por lo que una correcta configuración habilita tener un histórico de los cambios efectuados en las definiciones y poder así explotar posteriormente esta información.

## Vínculos

Relación de Documentos / Conceptos cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Estructura de Clientes Distribuidores](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/05-Estructura-Canal-de-Distribucion/DEFINICION-Estructura-Canales.md#titulo)

## Preguntas frecuentes

1. ¿Existe alguna premisa que deba ser tomada en consideración en la asignación de las Fuentes de Producción a los Agentes?

    En la [configuración de los Agentes](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/03-Agentes/DEFINICION-Agente.md), se puede especificar de manera voluntaria cual es la fuente de producción por defecto que el agente tiene asignada de la relación de fuentes de producción que éste tenga habilitadas.
    
## Audiencia

  - negocio
  - analista
  - implementador
  - desarrollador

[Referencia a los términos] 

[Canal de comercialización]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos-Comunes.md#canal-canal>

[Tabla TRON: A1000724]:<>