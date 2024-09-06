![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# CREAR movimiento diferido en Emisión ([enlace con visión técnica][Tecnica])

## **¿En que consiste?**
Esta acción supone el primer paso que se debe realizar para crear un proceso masivo. Esta acción además, es obligatoria realizarla.

## **Objetivo**
Genera la información necesaria que permitirá realizar un movimiento que se ejecutará de forma diferida.

## **Proceso a seguir**
En este caso hay indicar información a las siguientes propiedades:

![CREAR proceso masivo](./00-Imagen/CREAR-proceso-masivo-emision.png)

- [Propiedades generales](#propiedades-generales)
- [Propiedades que determinan la operación a realizar](#propiedadesoperacion)
- [Propiedades adicionales a la operación](#propiedadesadicionales)

## **Propiedades generales**
### **Compañía**
Entidad en la que se lanzará la [operación][Operacion] en diferido.

## **Propiedades que determinan la operación a realizar (Tipo)** {#propiedadesoperacion}
### **Movimiento a realizar**
Determina la [operación][Operacion] que se realizará en diferido. Los posibles movimientos se encuentran detalladas a continuación.

##### **Carga de presupuesto**
Genera un nueva propuesta, por lo que la [operación][Operacion] que se ejecuta es [EMITIR presupuesto][NoLink].

##### **Carga de póliza**
Genera una nueva póliza. La [operación][Operacion] que se ejecuta es [EMITIR póliza][EMITIR-poliza].

##### **Carga de aplicación**
Genera una nueva póliza con las condiciones de su póliza marco. La [operación][Operacion] que se ejecuta es [EMITIR aplicación][NoLink].

##### **Conversión de renovaciones**
Genera una póliza nueva simulando el proceso de renovación. Esto significa que, aunque se crea una nueva póliza, la [operación][Operacion] que se ejecuta no es de CREAR póliza, sino que se ejecuta la [operación][Operacion] [RENOVAR póliza][NoLink].

##### **Presupuesto de suplemento**
Genera una propuesta de nueva modificación. La [operación][Operacion] que se ejecuta es [EMITIR presupuesto de suplemento][NoLink].

##### **Presupuesto de suplemento aplicación**
Genera una propuesta de nueva modificación de aplicación. La [operación][Operacion] que se ejecuta es [EMITIR declaración][NoLink].

##### **Suplemento**
Genera una nueva modificación a una póliza. La [operación][Operacion] que se ejecuta es [ALTERAR póliza][NoLink].

##### **Suplemento de aplicación**
Genera una nueva modificación a una aplicación. La [operación][Operacion] que se ejecuta es [ALTERAR aplicación][NoLink].

##### **Renovación**
Genera un nuevo periodo de vigencia a una póliza. La [operación][Operacion] que se ejecuta es [RENOVAR póliza][NoLink].

##### **Anulación por falta de pago**
Genera uno o varios suplementos (por póliza),que cancelan total (la póliza) o parcialmente (el suplemento o los suplementos) la póliza debido a que los recibos generados tanto por nuevas pólizas, como por nuevos suplementos, el cliente no los ha pagado. Este proceso puede generar distintas [operaciones][Operacion]:

- [ANULAR póliza][NoLink]
- [ANULAR aplicación][NoLink]
- [ANULAR póliza modificación][NoLink]
- [ANULAR aplicación modificación][NoLink]

##### **Alterar Póliza desde presupuesto**
Genera una nueva modificación a una póliza con la información contenida en un presupuesto de un suplemento. La [operación][Operacion] que se ejecuta es [ALTERAR póliza][NoLink].

##### **Alterar aplicación desde presupuesto**
Genera una nueva modificación de una aplicación con la información contenida en un presupuesto de un suplemento. La [operación][Operacion] que se ejecuta es [ALTERAR aplicación][NoLink].

##### **Autoriza o rechaza control técnico póliza**
Permite la autorización o el rechazo de aquellas pólizas/aplicaciones que tienen errores y estos errores cuando se producen, alguna persona debe determinar si se permite o no la [operación][Operacion]. El proceso puede generar distintas [operaciones][Operacion]:

- [AUTORIZAR póliza][NoLink]
- [AUTORIZAR aplicación][NoLink]
- [RECHAZAR póliza][NoLink]
- [RECHAZAR aplicación][NoLink]

##### **Autoriza o rechaza control técnico presupuesto**
Permite la autorización o el rechazo de aquellos presupuestos que tienen errores y estos errores cuando se producen, alguna persona debe determinar si se permite o no la [operación][Operacion]. El proceso puede generar distintas [operaciones][Operacion]:

- [AUTORIZAR presupuesto][NoLink]
- [AUTORIZAR declaración][NoLink]
- [RECHAZAR presupuesto][NoLink]
- [RECHAZAR declaración][NoLink]

##### **Autoriza o rechaza control técnico pre-renovación**
Permite la autorización o el rechazo de aquellas [renovaciones previas][RenovacionPrevia] que tienen errores y estos errores cuando se producen, alguna persona debe determinar si se permite o no la [operación][Operacion]. El proceso puede generar distintas [operaciones][Operacion]:

- [AUTORIZAR pre-renovación][NoLink]
- [RECHAZAR pre-renovación][NoLink]

##### **Regularización vida**
Genera una nueva modificación a una póliza que permite el cálculo de la [prima de riego][PrimaRiesgo] en pólizas de [Unit Linked][UnitLinked]. La [operación][Operacion] que se ejecuta es [ALTERAR póliza][NoLink].

##### **Suspensión aportación pactada**
Genera una nueva modificación a una póliza suspendiendo el plan de aportación periódico cuando existe un número de aportaciones que el cliente no ha pagado. La [operación][Operacion] que se ejecuta es [ALTERAR póliza][NoLink].

##### **Recibos impagados**
Realiza el cambio de gestor de cobro a uno o varios recibos (por póliza) debido a que dichos recibos no han sido pagados. La operación que se ejecuta es [CAMBIAR recibo prima gestor][NoLink]

### **Fecha**
Esta fecha dependiendo de la [operación][Operacion] a realizar tiene mayor o menor relevancia a la hora de detallarla.

Por ejemplo, para el proceso:

- Cancelación por falta de pago. Indica el día en el que un recibo debe estar cobrado. Si un recibo no se encuentra cobrado a esa fecha, pasará al proceso de cancelación.
- Renovación. Determina cuando la póliza debe estar vencida. Si una póliza está vencida a esa fecha, pasa al proceso de renovación

## **Propiedades adicionales a la operación** {#propiedadesadicionales}
### **Orden**
El sistema permite crear más de un proceso masivo en una misma fecha. Esta propiedad es la que diferencia un proceso de otro en un mismo día. El valor cero (0) está reservado y no se debe utilizar.

### **Alias**
Permite crear una descripción que haga que el proceso masivo definido contenga información concreta. 

Por ejemplo, si se define un proceso masivo que renueve la cartera del mes de agosto, se puede especificar esta propiedad con esta información (Renovación de agosto).

### **Lógica de negocio de excepción (Objeto excepción)**
En este punto se puede asociar una [lógica de negocio][LogicaDeNegocio]. Esta lógica estará encargada de determinar que elementos se excluyen del proceso que se está definiendo. 

Por ejemplo, si se va a crear un proceso masivo con la renovación de la cartera de un mes y se desea que la cartera de un cliente quede excepcionada del proceso masivo porque se va a realizar un estudio y posterior renovación manual, se puede utilizar una lógica que haga esta tarea.

Esta lógica será lanzada justo antes de tratar la póliza. Es decir, si se está ejecutando un proceso masivo de renovación, esta lógica será lanzada antes de renovar la póliza. La lógica debe determinar si la póliza puede o no tratarse en el proceso masivo.

### **Aplica proceso estándar (Proceso estándar)**
El sistema permite dos modos en la creación de un proceso masivo:

- Estándar: Este proceso es libre. Cada usuario determina que pasos y en que orden (si se puede establecer) realiza la creación del proceso masivo
- Guiado: Este proceso, como su nombre indica está guiado y determina específicamente que pasos hay que seguir. para ello, necesita de una [DEFINICIÓN de proceso masivo de Emisión][NoLink]

### **Proceso personalizado**
Clave que enlaza el proceso personalizado que se asoció a proceso masivo que se está creando.

Este atributo determina el modo que seguirá este proceso masivo.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[LogicaDeNegocio]:  <../../../../../../99-Terminos/TRON-Terminos.md#logicadenegocio>
[Operacion]:        <../../../../../../99-Terminos/TRON-Terminos.md#operacion>
[RenovacionPrevia]: <../../../../../../99-Terminos/TRON-Terminos.md#renovacionprevia>
[UnitLinked]:       <../../../../../../99-Terminos/TRON-Terminos.md#UnitLinked>
[PrimaRiesgo]:      <../../../../../../99-Terminos/TRON-Terminos.md#primariesgo>

[Tecnica]: <./CREAR-proceso-masivo-emision-TECNICA.md>

[DEFINICIÓN de proceso masivo de Emisión]: <>

[ALTERAR aplicación]: <>
[ALTERAR póliza]: <>
[ANULAR aplicación]: <>
[ANULAR aplicación modificación]: <>
[ANULAR póliza]: <>
[ANULAR póliza modificación]: <>
[EMITIR aplicación]: <>
[EMITIR declaración]: <>
[EMITIR-poliza]: <../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/100-EMITIR-poliza/EMITIR-poliza.md>
[EMITIR presupuesto de suplemento]: <>
[EMITIR presupuesto]: <>
[RENOVAR póliza]: <>
[AUTORIZAR presupuesto]: <>
[AUTORIZAR declaración]: <>
[RECHAZAR presupuesto]: <>
[RECHAZAR declaración]: <>
[CAMBIAR recibo prima gestor]: <>
[NoLink]: <>