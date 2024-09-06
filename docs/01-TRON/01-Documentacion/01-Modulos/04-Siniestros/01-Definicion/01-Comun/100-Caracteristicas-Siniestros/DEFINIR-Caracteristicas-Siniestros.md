![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN Características del Módulo de Siniestros {#titulo}

<mark>Falta:</mark> Preguntas y respuestas, Link a documentos sin hacer, Revisar las lógicas

==EN CONSTRUCCIÓN==  

## **Objetivo**
La finalidad es definir el __comportamiento del sistema en los diferentes módulos de siniestros__.  
Se van a definir características comunes a todos los Ramos y Características específicas para cada Ramo. 

- [Propiedades Generales](#propiedades-generales)
- [Propiedades Ramo Procesos Automáticos](#propiedades-ramo-procesos-automaticos) 
- [Propiedades Ramo Apertura de Siniestros](#propiedades-ramo-apertura-siniestro) 
- [Propiedades Ramo Modificación de Siniestros](#propiedades-ramo-modificacion-del-siniestro) 
- [Propiedades Ramo Plan Tramitación](#propiedades-ramo-plan-de-tramitacion) 
- [Propiedades Ramo Juicios](#propiedades-ramo-juicios) 
- [Propiedades Ramo Liquidaciones](#propiedades-ramo-liquidaciones)

## **Propiedades Generales de Siniestros**  

### **Pedir Causas Apertura de Expedientes**
Este atributo indicará si cuando se __Apertura un expediente__, se van a pedir [las causas][causasexpedientes] de por qué se abre el expediente. Este valor aplicará a todos los expedientes independientemente del Ramo. Si se van a pedir causas de Apertura de Expedientes estas deberán estar definidas.


### **Pedir Causas Cambio de Valoración** {#pedircausascambiovaloracion}
Este atributo indicará si cuando se haga un __cambio de valoración de un expediente__, se van a pedir [las causas][causasexpedientes] de por qué se cambia la valoración. Este valor aplicará a todos los expedientes independientemente del Ramo.
Si se van a pedir causas del Cambio de Valoración de Expedientes estas deberán estar definidas.  
Consultar el documento de Definición de Causas

### **Pedir Causas Cambio de Valoración en Anulación de liquidación**{#pedircausascambiovaloracionanulacion}
Este atributo indicará si cuando se haga un __cambio de valoración__ de un expediente, provocado __por la anulación de una liquidación__ de ese expediente, se van a pedir[las causas][causasexpedientes] de por qué se cambia la valoración. Este valor aplicará a todos los expedientes independientemente del Ramo. 

Si se van a pedir causas del Cambio de Valoración de Expedientes estas deberán estar definidas.

### **Uso de Fecha de Control en el Plan de Tramitación** {#usofechadecontrol}
Este atributo permitirá o no que el __Plan de tramitación__ trabaje con __Fechas de control__. Esta fecha indicará al tramitador cuando debe finalizar la gestión que ha activado. Si se trabaja con Fechas de Control, se tendrá que definir para cada [trámite][definiciontramite] el número de días en los que se debería completar. La fecha se calculará desde el momento en el que el tramitador activa el trámite

[definiciontramite]:<NoLink>

Ejemplo: 

Si tenemos __trámites judiciales__ que se deben realizar en unos __plazos determinados__ por ley, el trámite que se encargue de realizar dichas tareas, se le podrá definir una fecha de control para que el tramitador, finalice la gestión en los plazos fijados por ley. Habrá consultas de todos los trámites que se encuentran fuera de plazo.

### **Uso de Roles en el Plan de Tramitación** {#usorolesplantramitacion}
En este atributo indicará si se va a __trabajar con Roles__, es decir, que ciertos trámites, sólo los puedan realizar determinados roles. En caso de que no se desee trabajar con roles, todos los tramitadores tendrán acceso a todo.  
La configuración de [roles][rolestramite] permite especializar más a los tramitadores y permitir que haya colaboradores que sólo tengan acceso a determinados trámites y trámites muy específicos que sólo los pueda ejecutar ciertos roles

Ejemplo :
	
Podemos tener a __tramitadores expertos en juicios__, que __sólo__ realicen ciertos __trámites judiciales__, o peritos que tengan acceso a trámites específicos de peritaciones.  

Estos roles afectan a estar operaciones del plan de tramitación:

- Activar Trámite
- Ejecutar programas asociados al trámite
- Generar comunicaciones asociadas al trámite
- Finalizar Trámite
- Retrasar Trámite
- Modificar Fecha control
- Incluir Trámite en el Plan
- Incluir Nivel en el Plan

[rolestramite]:<NoLink>

### **Uso de Calendarios en el Plan de Tramitación** {#usocalendarioplantramitacion}
Este atributo indica si en el Plan de Tramitación, __al calcular fechas se va a tener en cuenta los días festivos y vacaciones__ del tramitador o no.  Si se usa los [calendarios][calendarios], cuando se calculen las fechas, tendrá en cuenta los días festivos y las vacaciones, como días No hábiles. Si no se usa, todos los días serán hábiles.

 Esto afectará a las siguientes operaciones:
- Activar tramite con Aviso Definido
- Activar trámite con Fecha de control Definida
- Incluir aviso agenda en el Plan
- Modificar aviso, fecha de control…

[calendarios]:<NoLink>

### **Plan de Tramitación Solicitud de envío de Email** {#solicitudenvioemailplantramitacion}

Este atributo indicará, si cuando se envíe un email desde el Plan de Tramitación, se va a Informar al Plan, si el __envío del correo ha sido exitoso o fallido__.

### **Un Juicio puede afectar a Varios Siniestros**
Este atributo indica un juicio puede afectar a varios siniestros o no. El módulo de juicios permitirá asociar un siniestro o varios a un juicio, dependiendo del valor de este atributo.

### **Facturación Múltiple permite distribución Proporcional** {#permitedistribucionproporcionalfacturacionmultiple}
Este atributo indica si cuando se está distribuyendo el importe total de una Factura que afecta a múltiples expedientes (Factura de un profesional que interviene en varios expedientes) y el importe es igual para todos los expedientes si se va a permitir que eso lo haga automáticamente el sistema o si, por el contrario, se va tener que introducir manualmente este importe, para cada expediente.

Ejemplo: 
	
Si tenemos un perito que cobra un importe fijo por cada expediente, y el importe total es de 1000 y tenemos 10 expedientes, si se permite que el sistema distribuya el importe total automáticamente entre los 10 expedientes o se prefiere que el tramitador introduzca los 100 para cada expediente.

### **Facturación Múltiple Genera Liquidación con Expediente Retenido** {#generaliquidacionexpedienteretenido}
Este atributo indica si se va a permitir liquidar los conceptos de reserva tipo  Honorarios y Gastos, cuando el concepto que esté retenido es de tipo Indemnización. Es decir, permitir que se pague al profesional que ha intervenido en el Expediente, aunque la Indemnización esté retenida por Control Técnico. 

### **Valida Concepto de Pago en el Registro de Facturas**
Este atributo indica si cuando se está registrando un documento de pago de siniestros, en el Registro de Facturas, se valide que el concepto de cobro y pago vario que se introduce, esté definido para la actividad de la factura, o por el contrario, se va a registrar las facturas con conceptos genéricos.

## **Propiedades de Siniestros por Ramo**

Como se ha indicado anteriormente hay atributos que afectan a todos los ramos y atributos que pueden variar su comportamiento por ramo. En este apartado se detallará todos los atributos necesarios para el funcionamiento de Siniestros para cada Ramo. 

### **Ramo**
Este atributo indica la __[clave del Ramo][ramo]__ para el que se va a definir las características del módulo de Siniestros

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

## **Propiedades Ramo Procesos Automáticos** {#propiedades-ramo-procesos-automaticos}
Estas propiedades se definen por Ramo y son utilizadas en los procesos automáticos

### **Permite Apertura Automática de Expedientes** {#permite-apertura-automatica-de-expedientes}
Este atributo indica si __el Ramo va a permitir que se abran expedientes automáticamente__.   
Los Tipos de Expedientes que se pueden aperturar [automáticamente][tiposexpedientes] en el Ramo que se está definiendo, están detallados en la definición de tipos de Expedientes por Ramo.


### **Permite Apertura Automática de Expedientes desde Apertura de Siniestros on-line** {#permiteaperturaautomaticaexpedientesdesdeonline}
Este atributo indica si __el Ramo va a permitir que se abran expedientes automáticamente__ cuando estamos abriendo un __Siniestro manualmente__. Es decir cuando terminamos de introducir toda la información del siniestro, si se permite que el sistema intente abrir automáticamente todos los Tipos de Expedientes que se estén identificados como que se puedan abrir [automáticamente][tiposexpedientes] y cumplan las condiciones para ser abiertos.


### **Permite Apertura Automática de Expedientes desde Modificación de Siniestro** {#permiteaperturaautomativaexpedientesdesdemodificacion}

Este atributo indica si __el Ramo va a permitir que se abran expedientes automáticamente__ cuando estamos __modificando un siniestro__. Es decir cuando terminamos de modificar la información del siniestro, si se permite que el sistema intente abrir [automáticamente][tiposexpedientes] todos los Expedientes que se así estén definidos y que cumplan con las condiciones para que se puedan abrir.

Ejemplo:

Modificamos un siniestro para __incluir un lesionado__ que no estaba registrado. __Si este parámetro Es afirmativo__, el sistema irá a la definición de Tipos de Expedientes por Ramo e intentará abrir los expedientes que cumplan con las condiciones.  
En este caso si el Tipo de Expediente de Lesiones estuviera definido como posible apertura automática y __la información introducida cumpliera con los requisitos__ (por ejemplo, que esté informado el Tipo y Código de Documento del Lesionado), el sistema __abriría automáticamente un expediente de Lesiones__.

[tiposexpedientes]:<./DEFINIR-Tipo-Expediente.md#apertura-automatica>

### **Permite Aperturar Recobros desde la Apertura de Expedientes on-line**

Este atributo indica que, si estamos abriendo un Expediente cuyo Tipo de Expediente no es un Recobro y este, tiene definido que sus recobros se puedan abrir [automáticamente][recobrosautomaticos] __si se quiere que el sistema intente abrir automáticamente los Recobros asociado al Expediente que estamos abriendo__.

 [recobrosautomaticos]:<./DEFINIR-Recobros-por-Tipo-Expediente.md#aperturaautomatica>


## **Propiedades Ramo Apertura Siniestro**

### **Permite Siniestrar Póliza Marco** {#permitesiniestrarpolizamarco}
Este atributo indica si en la apertura de siniestros, cuando una póliza tiene póliza Marco, __si se permite que se siniestre dicha póliza Marco__ o sólo se pueden siniestrar las aplicaciones. Esto se utiliza para aquellos productos que tienen el comportamiento de transportes.

### **Permite Siniestrar Suplementos Temporales**
Este atributo indica al sistema __si se permite siniestrar un suplemento temporal__. Normalmente este atributo debería de ser afirmativo, ya que muchos suplementos temporales se hacen precisamente para reforzar la cobertura durante un tiempo, por si hay un siniestro. 

En algunas instalaciones para algunos ramos se han definido suplementos Temporales que son para cálculos internos o regularizaciones que no se quiere tener en cuenta a la hora de abrir un siniestro. 

Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación  

Ejemplo:

El asegurado se va de vacaciones y quiere aumentar la cobertura de robo en la póliza de su casa durante ese periodo. 
El asegurado se va de vacaciones al extranjero y quiere contratar durante el viaje, la cobertura de asistencia, Etc. 

Nota: Estos son suplementos temporales, que se deben tener en cuenta a la hora de abrir el siniestro.  

### **Permite Siniestrar Póliza No Vigente No transportes** {#permitepolizanovigentenotransportes}
  
Este atributo le indica a la apertura de siniestros, __si se permite siniestrar una póliza que, a la fecha del siniestro, no está vigente__.   
Esta propiedad sólo debería ser afirmativo en Ramos de Vida, ya que se puede anular la póliza por la muerte del asegurado, pero hay que abrir el siniestro y pagar a los beneficiarios.  
__La fecha del siniestro__ se corresponde con la fecha de la __muerte del asegurado__. 

Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación  

Nota: __Este caso, se da en las pólizas que sólo tienen un riesgo__. Si tuviera varios riesgos, lo que se anularía sería el riesgo.  

### **Permite Siniestrar Riesgo No Vigente No transportes**

Esta propiedad le indica a la apertura de siniestros, __si se permite siniestrar una póliza que, a la fecha del siniestro, no está vigente__.  
Este parámetro sólo debería ser afirmativo en Ramos de Vida, ya que se puede anular el riesgo por la muerte del asegurado, pero hay que abrir el siniestro y pagar a los beneficiarios.  
__La fecha del siniestro__ se corresponde con la fecha de la __muerte del asegurado.__de otros factores.  
Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación   

Nota: __Este caso, se da en las pólizas que tienen varios riesgos__. Si tuviera un riesgo, lo que se anularía sería la póliza.  

### **Permite Siniestrar Riesgo No Vigente Transportes**
Este atributo le indica a la apertura de siniestros si se permite siniestrar un Riesgo que no está vigente, en los Ramos de tratamiento de Transportes.  

Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación de otros factores.

 
Ejemplo:  
Esto puede ocurrir cuando en una póliza de transportes, se emiten __aplicaciones por cada viaje que se realice__. En el caso en el que se permita que estos __viajes puedan tener una duración mayor a la fecha de vencimiento de la póliza__. Se tiene que poner este atributo como positivo, ya que el viaje está asegurado, aunque el siniestro ocurra después de la fecha de vencimiento del Riesgo, si está dentro de la fecha del viaje declarada. 

### **Aperturar Siniestro sin Tipos de Expedientes Obligatorios**
Este atributo le indica a la apertura de siniestros, si se permite abrir un siniestro, si los tipos de expedientes que se han definido como obligatorios (para el Ramo, causa, consecuencia), no están abiertos. 

Normalmente esto se permite, cuando se quiere crear un control técnico y dejar retenido el siniestro, en vez de no dejar grabarlo

[Definición de Causa Consecuencia]()

### **Lógica que determina si se permite Aperturar Siniestro sin Tipos de Expedientes Obligatorios** 
Este atributo contendrá una lógica que determinará si se permite abrir el siniestro, si no se han abierto todos los Expedientes de los tipos que se han definido como [obligatorios][causaconsecuencias].  
Esta lógica se tendrá que definir, cuando no sea si o no, si que dependa de otros factores.

[causaconsecuencias]:<./DEFINIR-Causa-Consecuencias.md#obligatorio>

### **Permite Valorar Siniestro** 
Este atributo indica si cuando se abra el siniestro, se va a pedir una valoración global del mismo. Si no se permite, la apertura de siniestros no pedirá la valoración del siniestro.  

Ejemplo:  
Si en productos de Automóviles es el perito el que da el parte del siniestro, y este, está cualificado para dar una estimación de los daños del vehículo, se indicará mediante este atributo que se pida la valoración del siniestro.

### **Lógica que determina si se permite Valorar Siniestro**
Este atributo contendrá una lógica que indica si cuando se abra el siniestro, se va a pedir una valoración global del mismo. Si no se permite, la apertura de siniestros no pedirá la valoración del siniestro.  
Ejemplo:

Si en un producto de Automóviles es el perito el que da el parte del siniestro, y este, está cualificado para dar una estimación de los daños del vehículo, se indicará mediante este atributo que se pida la valoración del siniestro

### **Se pueden abrir siniestros a Futuro** {#permiteabrirsiniestrosafuturo} 
Este atributo indicará, indicará a la apertura de siniestros, si se va a permitir registrar un siniestro a futuro, es decir, si se puede __registrar un siniestro con una fecha de ocurrencia superior a la del día__.   

Los __valores permitidos__ serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación de otros factores.

Ejemplo:  

Esta propiedad se incluyó para los ramos de Salud. Cuando un asegurado pide una autorización para realizase una operación, hay compañías que lo registra en el sistema, ya que es un siniestro que va a ocurrir muy probablemente, con una fecha superior a la del día.

### **Valida Extemporaneidad**

Este atributo indicará al sistema, si se tiene en cuenta la [extemporaneidad][extemporaneidad] en el momento de abrir el siniestro, es decir, si se tendrá en cuenta el número máximo que puede transcurrir entre la fecha de ocurrencia del siniestro y la fecha de denuncia a la compañía.  

Los **valores permitidos** serán:  

-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación de otros factores.

Ejemplo:  

Puede haber algunos Ramos que, por sus características específicas, no haya fecha tope para informar un siniestro a la aseguradora, es decir que el siniestro nunca se declara fuera de plazo.  
En algunos ramos, se puede querer abrir el siniestro pero dejarlo retenido por Control Técnico en el caso de que se supere el número de días Máximo.

[extemporaneidad]:<./DEFINIR-Extemporaneidad.md#definiciondeextemporaneidad>

### **Lógica para obtener supervisor** {#logicaobtenersupervisor}
Este atributo contendrá la lógica de Negocio que determinará cuando se abra un siniestro, a que [supervisor][supervisor] se le debe asignar. Al iniciar siempre tenemos asignado la lógica de núcleo.

 La lógica de núcleo se apoya en varios catálogos:

1. Catálogo de definición del supervisor.
2. Catálogo de Relación entre las oficinas comerciales y tramitadoras.
3. Catálogo de Especialización de los supervisores.
4. Número de casos pendientes que tiene asignado el supervisor.  

[supervisor]:<NoLink>

### **Lógica para obtener descripción del Estado del Recibo** {#logicaparaobtenerestadodelrecibo}
Esta propiedad contendrá una lógica que en el caso de permitir que la póliza salga sin Recibo, la lógica le asigne una descripción.

Hay países que la póliza sale sin recibo y esta lógica devuelve SR- Sin Recibo

### **Lógica para obtener la persona de Contacto** {#logicaparaobtenerdatosdelcontacto}

Esta propiedad contiene una lógica que trata de traer todos los datos del contacto si estos están registrados en el Sistema.  
Esto se puede hacer ya que hay un atributo en la apertura del siniestro que te pide relación de la persona de Contacto con el Asegurado.  
Ejemplo: 
- Si el tipo de relación es el conductor, se irá a la póliza a extraer los datos del conductor
- Si el tipo de relación es el propietario, se irá a la póliza a extraer los datos del propietario...


### **Valida Causa-Consecuencia-Tipo de Expediente–Cobertura-Concepto de Reserva**

Esta propiedad indica a la apertura de siniestros, a la modificación y a la reapertura, si para la validación de  __consecuencias incompatibles__ dentro de un siniestro, se toma en cuenta Causa-Consecuencia- Tipo de Expediente y Cobertura o se baja esta validación a Causa-Consecuencia-Tipo de Expediente-Cobertura y Concepto de Reserva.  
Es decir, si esta propiedad es __No__, significa que __no__ se podrá elegir __dos consecuencias que afecten al mismo Tipo de Expediente, Cobertura__. Si esta propiedad es __SI__, significa que el control bajará a concepto de Reserva, es decir __no__ podrá seleccionarse __dos consecuencias que afecten al mismo Tipo de Expediente, Cobertura, Concepto de Reserva.__

Ejemplo:
__Causa__: 1001 Despiste

|Consecuencia | Tipo Expediente|	Cobertura | Concepto de Reserva
|---|---|---|---|
|1001 Daños Personales |LE- Lesionado| 100 Responsabilidad Civil Personal|1- Indemnización|
|1001 Daños Personales |LE- Lesionado| 100 Responsabilidad Civil Personal|2- Gastos|

- En este Ejemplo si la Marca es N, no se podrían marcar estas dos consecuencias, porque se validaría hasta Tipo de Expediente-Cobertura.   

- Si la Marca es Si, sí se podría marcar estas dos consecuencias porque la validación miraría hasta el Concepto de Reserva y el concepto de reserva es distinto.

### **Lógica para validaciones Propias al Final Apertura Siniestros** {#logicafinaldaperturasiniestros}

Este atributo contiene una lógica que permite a la instalación, añadir validaciones propias del País.


## **Propiedades Ramo Modificación del Siniestro** 

### **Permite Modificar Fecha del Siniestro**

Este atributo indicará al sistema, si se puede modificar la fecha de ocurrencia desde la modificación del siniestro.

Los **valores permitidos** serán:  
-    1: __Si__
-    2: __No__
-  3,4: __Lógica de Negocio__ se tendrá que definir una lógica de Negocio, si no siempre es Si o No, sino que dependa de la evaluación de otros factores.

Si se permite modificar la fecha, una vez modificada la fecha de ocurrencia del siniestro, la operación de Modificación de Siniestro, comprobará que no haya cambiado las condiciones de la póliza con respecto a la fecha que se introdujo anteriormente.   
Ejemplo:

__Fecha de Ocurrencia antes de la modificación__: 03-03-2023

|Póliza | Suplemento| Fecha Efecto	 | Fecha Vencimiento
|---|---|---|---|
|3082310100814|0 | 01-01-2023|01-01-2024|
|3082310100814|1 | 04-04-2023|01-01-2024|

Si se quiere Modificar la Fecha de Ocurrencia:

- Se puede modificar a cualquier fecha, si el siniestro no tiene expedientes abiertos.
- Se puede modificar la fecha de ocurrencia hasta el 31-03-2023, sin ningún problema ya que en este caso, sigue afectando al mismo suplemento.
- A partir del 4-04-2024, se podrá modificar siempre y cuando no afecte a los expedientes que ya están abiertos, es decir que se hayan des-contratado coberturas que ya tiene valoración o pagos

### **Permite Modificar Hora del Siniestro**
Este atributo indica si se permite modificar la hora del siniestro.  
Si en el ramo, el atributo de si se pide hora de vigencia es afirmativo, el programa de Modificación del siniestro, una vez modificada la hora, verificará que la póliza esté vigente a esa hora.   
Si la fecha del siniestro es la del día, verificará que no supere la hora del día.

### **Lógica para validaciones Propias al Final de Modificación de Siniestros** {#logicafinalmodificacionsiniestros}
Este atributo contiene una lógica que permite a la instalación, añadir validaciones propias del País.

## **Propiedades Ramo Plan de Tramitación**

### **Se Tipifican las Anotaciones Libres**

Las Anotaciones Libres, son Anotaciones que puede realizar el tramitador para dejar en el plan constancia de haber realizado una llamada, de cualquier circunstancia que quiera que quede reflejado en el Plan de Tramitación.

Esta propiedad indicará al Plan de tramitación si las [Anotaciones Libres][anotacioneslibres] se van a Tipificar, es decir que se van a definir previamente. Esto permite homogeneizar las anotaciones Libres. Si no se parametrizan el Tramitador podrá escribir lo que desee.

[anotacioneslibres]:<NoLInk>


### **Aviso al Plan Tramitación Desde el Módulo de Tesorería** {#avisoalplandesdetesoreri}

Este atributo indica si se quier recibir desde el módulo de tesorería, avisos en el plan de tramitación. Es decir cuando se pague una orden, se anule, etc, si este atributo es afirmativo,el sistema registrará un aviso en el Plan de tramitación, notificando de cualquier cambio en las órdenes de Pago del Siniestro- Expediente.


## **Propiedades Ramo Juicios**

### **Tipo y Código de Documento Obligatorio en Juicios** {tipocodigoobligatoriojuicios}

Este atributo indica si en el módulo de Juicios, cuando se piden las personas relacionadas con el Juicio, el tipo y el código van a ser obligatorios.

## **Propiedades Ramo Liquidaciones**

### **Traer datos Registro Factura**
Este atributo indica que si la liquidación (orden de pago) es de un documento que tiene que estar registrado en el Registro de Facturas, si al introducir los datos de la factura (proveedor, número y tipo de documento), se quiere que se traigan todos los datos registrados, a la liquidación.

### **Liquidar Documentos Oficial sin Registrar**
Este parámetro indica, si se deja generar la liquidación de un documento de pago tiene que estar en el registro de facturas y no está, o por el contrario, que no se deje generar la liquidación y de error.

### **Pedir cuenta Corriente en Liquidaciones**
Este atributo indica al sistema, si en el caso de no existir una cuenta registrada para el beneficiario de la liquidación, si se va a pedir la cuenta corriente o se da un error.

### **Cuenta Formateada**
Este atributo, indica si se muestra la cuenta corriente del beneficiario de la liquidación, formateada.

## **Propiedades Ramo Varios**

### **Datos Variables Compatibles**
Este atributo es para indica al sistema si la petición de datos variables, va a ser compatibles entre los dos sistemas NEWTron y TRONweb. Esto es sólo para instalaciones que tengan que convivir con los dos sistemas.

### **Consulta de siniestros Datos Adicionales**

## **Vínculos**

-

## **Preguntas frecuentes**
[Preguntas y respuestas relativas al concepto de negocio]


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
