![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN Tipo de Expediente {#titulo}

==EN CONSTRUCCIÓN==  
<mark>Falta:</mark> Preguntas y respuestas, Link a documentos sin hacer, Revisar las lógicas y los tipos
## **Objetivo**
La finalidad es definir todas las __tipologías de daños__ posibles, que se pueden producir a raíz de un siniestro. Se definirán los posibles daños ocasionados a nuestro asegurado, así como los daños que él haya podido causar a terceros.  

También se va a definir el __comportamiento__ de cada tipo de expedientes en los __diferentes ramos__ donde se pueda dar este tipo de daño, es decir, la información que se va a solicitar para ese tipo de expediente, si se puede peritar, si se puede asociar a un juicio, si es un recobro, etc. 


- [Propiedades Generales](#propiedades-generales)
- [Propiedades Generales Tipos de Expedientes Recobros](#propiedades-generales-tipos-de-expedientes-recobros)
- [Propiedades Generales Para Asignar Tramitador](#propiedades-generales-para-asignar-tramitador)
- [Propiedades Generales Validaciones Final Apertura](#propiedades-generales-validaciones-final-apertura)
- [Propiedades Por Ramo](#propiedades-por-ramo)
- [Propiedades Por Ramo para Procesos Automáticos](#propiedades-por-ramo-para-procesos-automaticos)
- [Propiedades Por Ramo para Uso de Módulos](#propiedades-por-ramo-uso-de-modulos)

## **Propiedades Generales** 
En este apartado se detallarán todos los atributos, propiedades comunes a todos los ramos, es decir los atributos que no cambian por ramo.

### **Tipo de Expediente**
Este atributo será __la clave__ por la que se va a identificar los distintos daños provocados por el siniestro.
Puede contener números y/o letras.

Una clave podrá ser utilizada para uno o varios ramos.      

Ejemplo: 

- Tipo de Expediente: __ROB__

Esta clave podría identificar a los expedientes, cuando el daño causado sea un Robo. Se podría utilizar para tramitar un expediente de una póliza de automóviles (robo del vehículo), o un expediente de una póliza de hogar (robo objetos en vivienda), etc.

- Tipo de Expediente: __DPA__
- Tipo de Expediente: __MUE__

### **Nombre del Tipo de Expediente**
Este atributo será la __descripción__ de la clave definida para el tipo de expediente. Puede contener números y/o letras.

Ejemplo: 

- Tipo de Expediente: __ROB__	Nombre del Tipo de Expediente: __Robo__
- Tipo de Expediente: __DPA__	Nombre del Tipo de Expediente: __Daños Por Agua__
- Tipo de Expediente: __MUE__	Nombre del Tipo de Expediente: __Muerte__  

### **Uso en Siniestros**

En este atributo se indicará si el tipo de expediente (tipo de daño) que se está definiendo, se va a utilizar en la tramitación de siniestros.  
Normalmente el tipo de expediente que se está definiendo será usado en la tramitación, esto se utiliza para casos extraordinarios.

Ejemplo:

- Tipo Expediente: ZZZ   Nombre: Todos los tipos de expedientes Uso en Siniestros: __N__

Este tipo de expediente se utiliza como genérico, no se va a utilizar en ningún proceso de siniestros.

### **Es Positivo**
Este atributo indica si el tipo de expediente es __positivo o es negativo__, es decir si el importe final del expediente va a ser positivo o negativo. Con esta definición el sistema controlará que el signo del importe del expediente se corresponda con lo definido.

### **Agrupar Tipos de Expedientes** 
Este atributo permite __agrupar__ a los tipos de expediente por su __naturaleza__. Es decir, se pueden agrupar todos los tipos de expedientes que tramiten daños materiales, o todos los tipos de expedientes que tramiten daños personales, o todos los tipos de expedientes que tramiten Robos, etc, independientemente de como se haya nombrado al tipo de daño.

Ejemplo: 

- Tipo de Expediente: LEC – Lesiones Conductor - Agrupación: __LE__ -Daños Personales
- Tipo de Expediente: LEO – Lesiones Ocupantes - Agrupación: __LE__ -Daños Personales
- Tipo de Expediente: DPL – Daños Propios Lunas - Agrupación: __DP__-Daños Propios
- Tipo de Expediente: DPM – Daños Propios Materiales - Agrupación: __DP__ -Daños Propios

Con este ejemplo, se podría sacar información de todos los expedientes cuya agrupación sea Daños Personales, independientemente de cómo se haya definido la clave, independientemente del Ramo. Lo mismo ocurriría con los expedientes de Daños Propios. 

### **Inhabilitado**
Este atributo indica si el Tipo de Expediente que está definido, está habilitado para poder abrir nuevos expedientes o si, por el contrario, ya no está habilitado para poder abrir nuevos expedientes con ese tipo de daño.

## **Propiedades Generales Tipos de Expedientes Recobros** 

Son propiedades de los Tipos de Expedientes de Recobro por Compañía, que no varían por Ramo.

### **Es un Recobro**
Este atributo indica si el tipo de expediente __es o no un recobro__.  
Los Recobros son tipos de expediente que se utilizan para recuperar parte del importe de un siniestro. Se puede recobrar a una compañía (cuando el tercero es culpable y tiene un seguro), se puede recobrar a un tercero (cuando este es culpable y no tiene seguro), se puede recobrar a un asegurado (cuando este tiene una franquicia contratada y la compañía ha adelantado el dinero) etc.

Ejemplo:

- Tipo de Expediente: 			REA
- Nombre Tipo de Expediente:	Recobro Asegurado 
- Uso en Siniestros:			S
- Tipo de Expediente es un Recobro:	__S__

### **Tipo de Recobro**

Este atributo sólo se informará en el caso de que el tipo de expediente sea un recobro. 
Lo que se va a definir es qué tipo de recobro es.  
Los Recobros pueden ser de tres tipos:

- __R__- Cuando son Recuperaciones Económicas
- __D__- Cuando se va a recuperar el Deducible (Franquicia) de un asegurado
- __S__- Cuando son Salvamentos (Recuperaciones Materiales) 

Si el recobro es de tipo Salvamento, este podrá tramitarse por el módulo de Salvamentos.  

### **Valorar Recobro con Valoración del Expediente principal** 
Este atributo sólo aplica cuando el expediente es un Recobro.  Indica si cuando se abra un recobro y se asocie a un expediente, el recobro toma la __valoración del expediente asociado__, o no.

### **Valorar el Recobro como el Expediente Principal**
Este atributo sólo aplica cuando el expediente es un Recobro.  
Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, cuando la valoración del recobro no es siempre la valoración del expediente al que está asociado, si no que depende de otros factores. Se tendrá que definir la lógica de Negocio que determine si toma la valoración del asociado o no.

Ejemplo:

Se abre un Recobro para solicitar a la Compañía contraria un importe y se le asocia, se le vincula con el expediente de Daños Propios del Vehículo Asegurado.
Se podría evaluar que, si la culpabilidad es del tercero, la valoración del recobro sea la valoración del expediente de Daños Propios Materiales, pero si la culpabilidad no es del contrario, la valoración la introduzca el tramitador.

### **Se permiten movimientos Positivos en Recobros**
Este atributo sólo aplica cuando el tipo de expediente que se está definiendo es un recobro.  

Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si el tipo de expediente permite en conceptos de reserva que no son Indemnización, valorar y pagar valores positivos. Puede ser Si o No, dependiendo de lo que se defina.  

Ejemplo: 

En un expediente de Recobro tipo Salvamento (Recuperación Material) se le puede indicar que permita importes positivos, pagar honorarios y gastos de los profesionales que intervinieron en el Recobro. Por ejemplo, para pagar a un abogado, a un recuperador. 

## **Propiedades Generales Para Asignar Tramitador** 

### **Asignar Tramitador en la Apertura de Expedientes** 

Este atributo contendrá la lógica de Negocio que determinará cuando se abra un expediente, a que __tramitador__ se le debe asignar. Existe una  lógica de núcleo

La lógica de núcleo se apoya en varios __catálogos__:

1. Catálogo de Definición del tramitador.
2. Catálogo de Relación entre las oficinas comerciales y tramitadoras.
3. Catálogo de Especialización de los tramitadores. 
4. Número de casos pendientes que tiene asignado el tramitador.
5. Número máximo de expedientes que se le puede asignar por día.

En el catálogo de __especialización__ de los tramitadores se le tiene que indicar si trabaja con los siniestros de:   

- Una o varias Estructuras Comerciales específicas
- Una o varias Pólizas Grupo, Contrato, Subcontrato.
- Uno o varios Sectores, Ramos, Agentes, Pólizas 
- Uno o varios Tipos de Expediente
- Expedientes en Juicio
- Expedientes de Pérdida Total 
- Expedientes ocurridos en el Extranjero
- Expedientes de Clientes VIP
- Expedientes Mapfre-Mapfre

Este atributo contendrá la lógica de Negocio que determinará cuando se abra un expediente, a que tramitador se le debe asignar.  
Al iniciar siempre estará asignado la lógica de núcleo.

- [Pendiente Definición Tramitador NO-LINK]

### **Asignar Tramitador en Reapertura de Expedientes** 

Este atributo contendrá la lógica de Negocio que determinará cuando se reapertura un expediente, a que tramitador se le debe asignar.

La lógica de núcleo se le asigna al tramitador original, que podrá ser cambiada.

## **Propiedades Generales Validaciones Final Apertura** 

### **Validaciones Final Apertura de Expedientes** 
Este atributo contendrá una lógica de Negocio, para poder realizar validaciones Extras.


## **Propiedades por Ramo**
Como se ha indicado anteriormente, los tipos de expedientes pueden tener diferente comportamiento por ramo.  
En este apartado se detallará todos los atributos necesarios para definir el comportamiento del tipo de expediente dentro de un Ramo.  
Se definirá que captura de datos va a tener asociado el tipo de expediente, que plan de tramitación (Procesos necesarios para tramitar correctamente el expediente), si se apertura automáticamente, etc.

### **Ramo**
Este atributo indica la clave del [Ramo][ramo] para el que se va a definir las características del tipo de expediente.

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Único por Siniestro** {#unico-por-siniestro}
Este atributo indica si ese tipo de expediente sólo puede abrirse una vez por siniestro.  

Ejemplo:   
Un Tipo de Expediente de __Pérdida Total__, sólo podrá haber __uno por siniestro__, un Tipo de Expediente de Muerte Conductor Asegurado sólo podrá haber uno por siniestro, sin embargo, el Tipo de expediente de Lesionados, No es único por siniestro, ya que puede haber varios lesionados dentro de un mismo Siniestro.

### **Moneda**
Este atributo indica la moneda con la que se va a valorar ese tipo de expediente.  
Para dar valor a este atributo se contará con la ayuda del catálogo de monedas.

Si se necesita que la moneda del expediente sea siempre la misma que la moneda de la póliza, se tendrá que introducir 99. Este valor indica al sistema que cuando se abra el expediente, tome la moneda de la póliza.

NOTA: La moneda del expediente, es independiente de la moneda con la que posteriormente se realicen los pagos de dicho expediente.

### **Moneda Única** {#moneda-unica}
Este atributo indica si la moneda que se ha definido en el atributo anterior, es la única moneda permitida para el Tipo de Expediente.
- Si se indica que, __SI es única__, el tramitador __no podrá cambiar__ el valor de la __moneda__ cuando abra un expediente. 
- Si se indica que __No es única__, el tramitador __podrá cambiar__ el valor de la __moneda__ cuando se abra un expediente.

### **Información para el Tipo de Expediente** {#informacion-para-el-tipo-de-expediente}
Este atributo indica los datos que se van a pedir cuando se abra un expediente del Tipo que se está definiendo.   
Para cada tipo de expediente habrá que determinar toda la información que se va a requerir, para cada propiedad habrá que indicar:

- Longitud: número de posiciones.
- Tipo: Numérico, alfanumérico, fecha…
- Obligatoriedad: si es o no obligatorio, o las condiciones para que este dato sea obligatorio.
- Validación: si está codificado en un catálogo, ver si existe el código en dicho catálogo…
- Valor Inicial: Si se quiere que el sistema cuando pida la información ya tenga un valor inicial, etc.

A toda esa información (conjunto de propiedades, atributos) se le dará una clave y un nombre y dicha clave se asociará al Tipo de Expediente en este atributo.

Se le puede indicar sin datos, utilizando el valor genérico.

Ejemplo:

Un Tipo de Expediente de Lesiones con la __estructura de información 1__

Clave de Estructura de información: 1  
Nombre de Estructura de información: Datos del Lesionado  
Atributos:  

- Documento identificativo:  tres posiciones, alfanumérico, validado contra el catálogo de tipos de documentos de la compañía. No es Obligatorio.  
- Número de Documento Identificativo. 12 posiciones, alfanumérico, validado contra la validación de documentos de la compañía. Es obligatorio si se introduce información en el Documento identificativo.  
- Nombre del Lesionado:  60 posiciones, alfanumérico, Sin validación, Obligatorio.  
- Apellidos del Lesionado: 60 posiciones, alfanumérico, Sin validación, Obligatorio.  
- Teléfono de Contacto:  
- Tipo de Lesión:  3 posiciones, alfanumérico, valores posibles: L- Leve, M- Moderado, G- Grave.

Lo que significa esto es que cuando se abra un expediente de tipo Lesiones, el sistema pedirá todos los atributos que tenga asociados la estructura de datos 1.  

 [Definición Estructura Tipo Expediente NOLINK]

### **Lógica que determina la información del Tipo de Expediente** {#logica-que-determina-la-informacion-del-tipo-de-expediente}
Este atributo contendrá una lógica de Negocio, cuando la información que recoge los datos no es fija por tipo de expediente, sino que depende de otros factores.  
Se tendrá que definir la lógica de Negocio que determine la información que se va a solicitar, para tramitar ese tipo de daño. 

Ejemplo:  
Se ha definido un tipo de Expediente para tramitar todos los daños propios del vehículo, pero se cuenta con dos estructuras para recoger esta información, una para pedir los datos cuando el daño es una Pérdida Total, y otra cuando el daño es una Pérdida Parcial. En este caso se podría definir una lógica de Negocio, que determine que, si la consecuencia seleccionada es una pérdida total, se pida la información de una pérdida total, en caso contrario, se pida la información de pérdida parcial.

### **Plan de Tramitación** {#plantramitacion}
Este atributo indicará el plan de tramitación que se encargará de realizar todas las gestiones necesarias desde la apertura del expediente, hasta su cierre. Se facilitará la ayuda de los planes de tramitación definidos.

Puede haber tipos de Expedientes que por su naturaleza no necesiten un plan de tramitación o que el plan no sea siempre el mismo y dependa de otros factores.

### **Lógica que determina el Plan de Tramitación** {#Logica-plan-Tramitacion}
Este atributo contendrá una lógica de Negocio, cuando el plan de tramitación no es fijo por tipo de expediente, sino que depende de otros factores. Se tendrá que definir la __lógica__ de Negocio que __determine el código del plan__ que se va a utilizar, para tramitar este tipo de daño.

Ejemplo:  
Se ha definido un tipo de Expediente para tramitar todos los daños propios del vehículo, pero se cuenta con dos planes de tramitación, uno para gestionar cuando el daño es una Pérdida Total, y otro para gestionar cuando el daño es una Pérdida Parcial. En este caso se podría definir una lógica de Negocio, que determine que, si la consecuencia seleccionada es una pérdida total, se tome el plan de tramitación de pérdida total, en caso contrario, se le asocie al expediente el plan de tramitación de pérdida parcial.

### **Calcula Reserva**
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, se __tiene en cuenta o no__, en el __cálculo de reservas de fin de mes__. Cuando haya otros factores además del Tipo de Expediente que determine si entra o no entra, se tendrá que definir una lógica de Negocio.

### **Lógica que determina si Calcula Reserva** {#Logica-que-determina-si-Calcula-Reserva}
Este atributo contendrá una __lógica__ de Negocio, que determinará si los expedientes con este tipo de daño se __tienen en cuenta o no__, para el __cálculo de reservas de fin de mes__. Se tendrá que definir esta lógica cuando no dependa únicamente del tipo de daño, sino de otros factores.

### **Causas de Apertura**
Este atributo indicará si se quiere __pedir las causas de apertura__ de un expediente, cuando este sea del tipo de daño que se está definiendo. Si se indica que sí, habrá que definir las causas de Apertura de Expedientes para el Tipo de Expediente del Ramo que se está definiendo.

### **Valoración Ajustada** {#valoracion-ajustada}
Este atributo indicará si al abrir un expediente de este tipo manualmente, se le va a permitir al tramitador indicar una __reserva inicial manualmente__, o si por el contrario siempre se va a abrir por la reserva promedio definida previamente, sin poder modificarla el tramitador.


## **Propiedades por Ramo Uso de Módulos** {#propiedades-por-ramo-uso-de-modulos}

### **Juicio**
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, __puede ser asociado a un juicio__. Cuando se registre un juicio, y se le vaya a asociar expedientes, sólo se mostrarán los expedientes cuyo Tipo de Expediente tenga la Marca de Juicio.

### **Varios Juicios**
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, puede ser __asociado a varios juicios.__

### **Peritación** {#peritacion}
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, se le __puede realizar una peritación__. Sólo se podrá solicitar una peritación, a los expedientes cuyo Tipo tenga la Marca de Peritación.

Ejemplo:  

Si se define un Tipo de Expediente LEO- Lesionado Ocupantes, los expedientes que sean de este tipo no se les deberá peritar, puesto que será un expediente para tramitar lesiones. Sin embargo, si se ha definido un Tipo de Expediente DP-Daños Propios del vehículo, este Tipo de Expediente tramitará los daños Materiales y si es factible a realizarle una peritación.

### **Peritación Obligatoria** {peritacion-obligatoria}
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, es __obligatorio realizarle una peritación__. Esta información se solicitará, si se tipo de expediente puede tener peritación. Si se indica que es obligatorio tener una peritación, no se dejará realizar liquidaciones, hasta que no se realice dicha peritación.
Ejemplo:

Si se ha definido un Tipo de Expediente LEO- Lesionado Ocupantes, los expedientes que sean de este tipo no se les deberá peritar, puesto que será un expediente para tramitar lesiones. Sin embargo, si se ha definido un Tipo de Expediente DP-Daños Propios del vehículo, este Tipo de Expediente tramitará los daños Materiales y si es factible a realizarle una peritación

### **Lógica que determina si Peritación Obligatoria**
Este atributo contendrá una lógica de Negocio, que __determinará__ si los expedientes con este tipo de daño, es __obligatorio o no__, realizar la __peritación__. Se tendrá que definir esta lógica cuando no dependa únicamente del tipo de daño, sino de otros factores. 
Ejemplo:

Se ha definido un tipo de Expediente de Daños Propios Materiales.  
Se quiere que este tipo de expediente, si la __consecuencia es Lunas__, __no sea obligatoria la peritación__ y en los demás casos si sea obligatoria. En este caso no depende sólo del tipo de daños, sino de las consecuencias que se hayan seleccionado previamente.

### **Facturación** {#facturacion}
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, se va a tramitar sus importes económicos __a través del módulo de Facturación__. Esto se suele utilizar sobre todo para los tipos de Expedientes de Salud.  

### **Plan de Renta Mensual**
Este atributo indicará si un expediente con el Tipo de Daño que se está definiendo, se va a __gestionar por un Plan de Renta Mensual__. Esto se suele utilizar sobre todo para los tipos de Accidentes Personales o Accidentes Laborales.

## **Propiedades por Ramo para Procesos Automáticos** {#propiedades-por-ramo-para-procesos-automaticos}  

### **Apertura Automática** {#apertura-automatica}

Este atributo indica si el tipo de expediente que se está definiendo, se va a __permitir aperturar automáticamente__, siempre que se elija la causa consecuencia que permita abrirlo.   
Cuando se apertura automáticamente, se abre por la reserva inicial definida para el Ramo, causa, consecuencia, Tipo de Expediente, concepto de reserva, cobertura.

### **Lógica que determina Apertura Automática**
Este atributo contendrá una lógica de Negocio, cuando no siempre se abre o no se abre automáticamente, sino que va a depender de otros factores que no son el tipo de expediente que se está definiendo. Se tendrá que definir la __lógica__ de Negocio que __determine si se abre o no automáticamente__.

Ejemplo:

Si se ha indicado que el siniestro tiene como consecuencia daños personales, se puede definir una lógica que evalúe que, si se ha informado el nombre, apellidos y documento identificativo del lesionado, se abra automáticamente, sino no se abra automáticamente.

Si se ha indicado que el siniestro tiene como consecuencia daños vehículo contrario, se puede definir una lógica que evalúe que, si se ha informado la placa o matrícula del vehículo contrario se abra automáticamente, sino no se abra automáticamente.

### **Lógica que determina Número de Expedientes a abrir automáticamente**
Este atributo sólo se pedirá si está activada la apertura automática del tipo de expediente que se está definiendo o si se ha definido una lógica para determinar si se abre o no automáticamente. Este atributo contendrá una __lógica__ de Negocio, que devolverá el __número de expedientes__ que se va a abrir automáticamente de ese tipo.

Nota: Si el tipo de Expediente es único por siniestro (Robo Total, Pérdida Total), sólo se podrá abrir uno.

Ejemplo: 

Si se ha indicado que el siniestro tiene como consecuencia daños personales, se puede definir una lógica que evalúe que, cuántos lesionados se han informado en el parte y se abran tantos expedientes, como lesionados haya o que se abran sólo los lesionados que tengan documento de identidad, nombre y apellidos.

Si se ha indicado que el siniestro tiene como consecuencia daños vehículo contrario, se puede definir una lógica que evalúe que, si se ha informado la placa del vehículo contrario se abra automáticamente tantos expedientes como vehículos contrarios tengan matrícula o placa.

### **Lógica que determina Aviso Apertura de Expediente**
Este atributo contendrá una lógica de Negocio, que devolverá el __Aviso que se quiere mostrar al tramitador__, cuando se le asigne un expediente nuevo abierto manual o automáticamente.

Ejemplo: 

Actualmente existen varias lógicas de núcleo. Hay una para Daños Materiales y para Daños Personales que devuelve:

Tipo de Expediente-Nombre y Apellidos del propietario del vehículo o lesionado-Oficina Tramitadora- Oficina Gestora-Tramitador-Supervisor

__Daños Materiales Contrarios:__ Pelayo del Monte Alto 
__Oficina tramitadora__: 1101 - __Comercial:__ 1101 Oficina Comercial Centro 
__Tramitador:__ 105 – Aurelio Manzano, __Supervisor:__ Mariana Fernández


### **Tipo de Aviso de Reasignación de Expediente**
Este atributo contendrá el subtipo de Aviso que se quiere mostrar al tramitador, cuando se le asigne un expediente manual o automáticamente, que estaba tramitando otro tramitador.


Ejemplo: 

En núcleo se tiene definido el tipo de aviso ‘RT’- Reasignación de Tramitador. 

### **Aviso en la Modificación de Expediente**
Este atributo contendrá si se genera o no se genera aviso en la modificación de Expediente.
Los valores posibles son:   

- **1** No genera aviso en la modificación de Expediente 
- **2** Si genera aviso en la modificación de Expediente 

### **Lógica que determina Aviso Modificación de Expediente**
En el caso en el que el atributo anterior sea un 2 (genera aviso en la modificación del expediente), este atributo contendrá una __lógica__ de Negocio, que devolverá el __Aviso que se quiere mostrar al tramitador__, cuando se modifique un expediente manual o automáticamente. Este atributo será obligatorio, siempre y cuando el tipo de aviso de modificación de expediente sea ‘2’.  

Ejemplo:

Un posible aviso podría ser :  
Modificado: Tipo de Expediente-Usuario que realizó Modificación- Fecha de Modificación-  
__Modificado:__ DPA- __Usuario:__ MPP- María Pérez Pérez __Fecha de Modificación:__ 20-mayo-2023

### **Tipo de Termina Tramites**

Este atributo contendrá que acción se debe realizar con todo lo que hay pendiente en el Plan de tramitación de un expediente, cuando este se termina. Es decir, cuando se termina un expediente manual o automáticamente, qué hacer con los trámites pendientes, con los avisos pendientes, etc.

Los valores posibles son:  

- __N__	No se finaliza Nada   
- __D__	Finaliza trámites Definidos Pendientes  
- __A__	Finaliza Avisos Pendientes  
- __T__	Finaliza Todo  

Para entender mejor el concepto de Tipo de Expediente sería recomendable leer el documento de definición de siniestro – expediente.
## **Vínculos**

- [Definición de Siniestro-Expediente](https://mapfrecorp-my.sharepoint.com/wiki/spaces/CTRON/pages/8714739870914085337)


## **Preguntas frecuentes**
[Preguntas y respuestas relativas al concepto de negocio]  

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

