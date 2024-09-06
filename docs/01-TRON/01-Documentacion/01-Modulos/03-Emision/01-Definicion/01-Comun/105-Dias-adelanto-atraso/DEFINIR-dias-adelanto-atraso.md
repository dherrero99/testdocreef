![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# DEFINICIÓN de días de adelanto y atraso {#titulo}

## **Objetivo**

Existe la posibilidad de controlar el número de días con los que se puede realizar un [tipo de movimiento][tip-emision] en emisión de forma adelantada o con retraso. Un ejemplo de definición podría ser el siguiente:

| DÍAS DE RETRASO | DÍAS DE ADELANTO |
| :---:            | :---:           |
| 30               | 15              |

Suponiendo que en el ejemplo el día es **01-Septiembre-2023**, esta definición limita el efecto a:

``` mermaid
graph LR
  A["02-Agosto-2023"]
  B["01-Septiembre-2023"]
  C["16-Septiembre-2023"]
  B -- "retraso (30 días)" --> A;
  B -- "adelanto (15 días)" --> C;
```

Es decir, suponiendo que el objetivo es emitir una nueva póliza, según el ejemplo el efecto puede estar entre el día **2 de agosto de 2023** y el día **16 de septiembre de 2023**.

-[Propiedades generales](#propiedades-generales)  
-[Propiedades generales](#otras-propiedades)


## **Propiedades generales** {#propiedades-generales}
### **Ramo**
Indica al [ramo][ramo] que afecta la definición.

### **Póliza grupo**
Si se especifica, la definición aplicará cuando se realice un [tipo de movimiento][tip-emision] que contenga la información del atributo.

### **Contrato**
Si se especifica, la definición aplicará cuando se realice un [tipo de movimiento][tip-emision] que contenga la información del atributo.

### **Subcontrato**
Si se especifica, la definición aplicará cuando se realice un [tipo de movimiento][tip-emision] que contenga la información del atributo.

### **Tipo de emisión**
Determina el [tipo de movimiento][tip-emision] afectado.

### **Número de días de adelanto**
Especifica cuantos días se puede realizar un [movimiento][tip-emision] por adelantado.

### **Número de días de retraso**
Especifica cuantos días se puede realizar un [movimiento][tip-emision] con retraso.

## Otras Propiedades {#otras-propiedades}
### **Inhabilitación**
Especifica si la definición está activa o no.

### **Fecha de validez**
Indica a partir de cuando la definición es efectiva.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[tip-emision]:        <../../../../../../99-Terminos/TRON-tipo-emision.md#tip-emision>
[ramo]:               <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>