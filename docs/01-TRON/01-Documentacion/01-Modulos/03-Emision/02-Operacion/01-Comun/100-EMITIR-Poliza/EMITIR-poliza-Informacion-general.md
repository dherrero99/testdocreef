![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# EMITIR póliza - Información básica y general de póliza

## **¿En que consiste?**
Información requerida y que afecta a todos los riesgos que pueda contener la póliza.

## **Objetivo**
Conocer que información puede solicitarse en este nivel dependiendo de la definición del [ramo][ramo].

## **Proceso a seguir**
A continuación detallan las propiedades que pueden participar en esta operación.

- [Propiedades de información previa](#informacion-previa)
- [Propiedades de información básica](#informacion-basica)
- [Propiedades de información general](#informacion-general)

## **Información previa** {#informacion-previa}
### **Ramo**
Identifica el riesgo (o riesgos) que se va a asegurar. La [definición][ramo] contiene todas las características que el proceso de emisión tendrá en cuenta.

## **Información básica** {#informacion-basica}
### **Póliza grupo**
Especifica si la póliza que se va a emitir se adhiere a un [grupo][poliza-grupo] o no.

### **Contrato**
Identifica si la póliza tiene [condiciones][contrato] especiales.

### **Subcontrato**
Establece si la póliza tiene [condiciones][subcontrato] específicas para el [contrato][contrato] dado. Esto es posible si se ha seleccionado un contrato.

### **Nº de póliza**
Contiene el [identificador][numero-de-poliza] de la póliza que se está emitiendo. Este número puede ser tomado de forma automática o puede haber sido reservado previamente.

### **Tipo de póliza**
Este [tipo][tip-poliza-tr] es un atributo específico de trasportes. Para los ramos con un [tratamiento][tratamiento] distinto, el valor es "FIJO".

### **Fecha de efecto**
Especifica la fecha en la que comienza la cobertura del riesgo (o riesgos). Esta fecha puede limitarse mediante [definición][dias-adelanto-atraso].

### **Fecha de vencimiento**
Contiene la fecha en la que la póliza vence. Adicionalmente, detesta fecha influye en la [duración][tip-duracion] de la póliza.

## **Información general** {#informacion-general}
### **Moneda**
Establece la [divisa][moneda] de la póliza. Este atributo afecta a varios conceptos:

- [Capital de la cobertura][NoLink]  
- [Franquicia de la cobertura][NoLink]  
- [Conceptos de desglose][NoLink]  
- [Comisiones][NoLink]  
- [Conceptos económicos][NoLink]  
- [Recibos][NoLink]  

### **Tipo de cambio**
Muestra el valor de la conversión entre la moneda elegida de la póliza respecto a la moneda del país. Este valor influye en toda la información económica de la póliza. Este atributo puede ser modificable o no por [definición][tipo-cambio].

### **Renovable**
Determina si la [duración][tip-duracion] de la póliza será [anual prorrogable][anual-prorrogable].

### **Renovable temporalidad**
Determina si la [duración][tip-duracion] de la póliza será [Temporal renovable por su temporalidad][temporal-temporalidad]. Esto ocurre cuando  los días entre el efecto y el vencimiento de la póliza es menor a un año.

### **Renovable periodicidad**
Determina si la [duración][tip-duracion] de la póliza será [Temporal renovable por su periodicidad][temporal-periodo]. Esto ocurre cuando  los días entre el efecto y el vencimiento de la póliza es menor a un año.

### **Nº de renovaciones**
Se puede fijar el número máximo de renovaciones que la póliza tendrá si la póliza se renueva. Si se deja con el valor por defecto (cero), la póliza se renovará indefinidamente hasta que se anule.

Por ejemplo, suponiendo que la póliza tiene una [duración][tip-duracion] que implica la renovación, el valor de este atributo indicará el número de renovaciones que tendrá la póliza.

| Nº DE RENOVACIONES | CONSECUENCIA |
| :---:              | :---         |
| 0   | Se renovará hasta que se anule |
| 1   | Se renovará una vez y solo una vez |
| 020 | Se renovará veinte veces |
| 100 | Se renovará cien veces |

### **Tipo de revalorización del riesgo**
Se activa en el caso que la definición del ramo determine que alguna cobertura, la forma en la que revaloriza, se decida en el momento de la emisión de la póliza. El tipo de revalorización elegido afectará a todas las coberturas que tienen esta definición.
### **Porcentaje de revalorización del riesgo**
### **Índice de revalorización del riesgo**
### **Prima manual**
### **Cálculo a prorrata**
### **Nº de póliza cliente**
### **Tipo de negocio**
### **Tipo de envío**
### **Tipo de reaseguro**
### **Reaseguro manual**
### **Reaseguro marco**

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[poliza-grupo]:             <../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/01-Definicion/01-Comun/101-Poliza-Grupo/DEFINIR-poliza-grupo.md#titulo>
[contrato]:                 <../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/01-Definicion/01-Comun/102-Contrato/DEFINIR-contrato.md#titulo>
[subcontrato]:              <../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/01-Definicion/01-Comun/103-Subcontrato/DEFINIR-subcontrato.md#titulo>
[numero-de-poliza]:         <../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/01-Definicion/01-Comun/104-Numero-de-poliza/DEFINIR-formato-numero-poliza.md#titulo>
[dias-adelanto-atraso]:     <../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/01-Definicion/01-Comun/105-Dias-adelanto-atraso/DEFINIR-dias-adelanto-atraso.md#titulo>
[ramo]:                     <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>
[moneda]:                   <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/01-Moneda/DEFINICION-de-Moneda.md#titulo>
[tratamiento]:              <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#tratamiento-emision>
[tipo-cambio]:              <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#modificar-tipo-de-cambio>
[tip-poliza-tr]:            <../../../../../../../01-TRON/99-Terminos/TRON-tipo-emision.md#tip-poliza-tr>
[tip-duracion]:             <../../../../../../../01-TRON/99-Terminos/TRON-tipo-emision.md#tip-duracion>
[anual-prorrogable]:        <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#anual-prorrogable>
[temporal-temporalidad]:    <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#temporal-renovable-temporalidad>
[temporal-periodo]:         <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#temporal-renovable-periodo>

[cobertura-capital]:        <>
[cobertura-franquicia]:     <>
[concepto-desglose]:        <>
[comision]:                 <>
[concepto-economico]:       <>
[recibo]:                   <>

[NoLink]: <>