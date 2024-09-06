![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

# CREAR movimiento diferido en Siniestros ([enlace con visión técnica][Tecnica]) {#titulo}

## **¿En que consiste?**
Esta acción supone el primer paso que se debe realizar para crear un proceso masivo. Esta acción además, es obligatoria realizarla.

## **Objetivo**
Genera la información necesaria que permitirá realizar un movimiento que se ejecutará de forma diferida.

## **Proceso a seguir**
En este caso hay indicar información a las siguientes propiedades:

[CREAR proceso masivo Siniestros]()

- [Propiedades generales](#propiedades-generales)
- [Propiedades que determinan la operación a realizar](#propiedadesoperacion)
- [Propiedades adicionales a la operación](#propiedadesadicionales)

## **Propiedades generales**
### **Compañía**
Entidad en la que se lanzará la [operación][Operacion] en diferido.

## **Propiedades que determinan la operación a realizar (Tipo)**  {#propiedadesoperacion}

### **Movimiento a realizar**
Determina la [operación][Operacion] que se realizará en diferido.  
Los posibles movimientos se encuentran detallados a continuación:  
#### **10 Apertura de Siniestro**  
Abre un siniestro e intenta abrir expedientes, por lo que la [operación][Operacion] que se ejecuta es [APERTURAR siniestro][NoLink].  

#### **11 Modificación de Siniestro**  
Modifica los datos de un siniestro, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR siniestro][NoLink].  

#### **12 Terminación de Siniestro**  
Termina siniestros que no tengan expedientes, por lo que la [operación][Operacion] que se ejecuta es [TERMINAR siniestro][NoLink].  

#### **14 Rehabilitación de Siniestro**   
Rehabilita un siniestro que está terminado, para incluir un nuevo expediente, por lo que la [operación][Operacion] que se ejecuta es [REHABILITAR siniestro][NoLink].  

#### **20 Apertura de Expediente desde el Batch de Siniestros**  
Abre un nuevo expediente con valoración promedio. Este proceso ejecuta varias  [operaciones][Operacion]:

- [APERTURAR expediente desde Batch de Siniestros][NoLink]. 
- [CREAR valoración Expediente][NoLink] 

#### **21 Apertura de Expediente**  
Abre un nuevo expediente con valoración promedio. Este proceso ejecuta distintas [operaciones][Operacion]:

- [APERTURAR expediente][NoLink].  
- [CREAR valoración Expediente][NoLink]

#### **22 Modificación de Expediente**    
Modifica sólo los datos de un expediente, por lo que la [operación][Operacion] que se ejecuta es 
[MODIFICAR expediente][NoLink].  

#### **23 Terminación de Expediente**  
Termina expedientes, por lo que la [operación][Operacion] que se ejecuta es [TERMINAR expediente][NoLink].  

#### **24 Rehabilitación de Expediente**  
Rehabilita un expediente que está terminado, por lo que la [operación][Operacion] que se ejecuta es [REHABILITAR expediente][NoLink].  

#### **25 Cambio de Valoración de Expediente**   
Modifica la valoración de un expediente que está pendiente, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR valoración expediente][NoLink].  

#### **30 Liquidación de Expediente**  
Genera una liquidación de expediente, una orden de pago, por lo que la [operación][Operacion] que se ejecuta es [LIQUIDAR expediente][NoLink].  

#### **31 Rectificación de Liquidación**    
Modifica una liquidación de expediente y la orden de pago, siempre y cuando no esté pagada, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR liquidación][NoLink].  

#### **32 Anulación de Liquidación**  
Anula una liquidación de expediente y la orden de pago, siempre y cuando no esté pagada, por lo que la [operación][Operacion] que se ejecuta es [ANULAR liquidación][NoLink]. 

#### **33 Justificante suelto (Liquidación a Expediente Terminado)**  
Genera una liquidación, cuando el expediente está terminado por lo que la [operación][Operacion] que se ejecuta es [GENERAR liquidación][NoLink].
 
#### **40 Crear Aviso**  
Genera un nuevo Aviso en el plan de tramitación de un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR aviso][NoLink].  

#### **41 Crear Anotaciones Libres**  
Genera una Anotación libre en el plan de tramitación de un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR anotación][NoLink].  

#### **42 Crear Nivel en el Plan**  
Genera un nivel en el plan de tramitación de un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR nivel][NoLink].  

#### **43 Crear Trámite en el Plan**    
Genera un trámite en el plan de tramitación de un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR trámite][NoLink].  

#### **44 Reasignar Tramitador Expediente**   
Cambia el tramitador de un expediente, por lo que la [operación][Operacion] que se ejecuta es [REASIGNAR tramitador][NoLink]. 

#### **46 Finalizar Trámite Pendiente**  
Finaliza un trámite del plan de tramitación de un expediente, por lo que la [operación][Operacion] que se ejecuta es [FINALIZAR trámite][NoLink].  

#### **50 Plan de Renta Mensual**  
Crea un Plan de Renta Mensual a un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR plan de renta mensual][NoLink]. 

#### **51 Anulación de un P.R.M.**    
Anula el Plan de Renta Mensual de un expediente, por lo que la [operación][Operacion] que se ejecuta es [ANULAR plan de renta][NoLink]. 

#### **52 Terminación de un P.R.M.**   
Termina el Plan de Renta Mensual de un expediente, por lo que la [operación][Operacion] que se ejecuta es [TERMINAR plan de renta][NoLink].  

#### **53 Terminación de un P.R.M. sin anular**  
Termina un plan de Renta Mensual de un expediente sin anularlo, por lo que la [operación][Operacion] que se ejecuta es [TERMINAR plan de renta sin anular][NoLink]. 

#### **60 Solicitud y Resultado de la Peritación** 

Crea la solicitud de la peritación o la modifica si ya existe, también puede crear el resultado de la misma o modificar el resultado si no estuviera informado. Este proceso puede generar distintas [operaciones][Operacion]:

- [CREAR solicitud peritacion][NoLink]
- [MODIFICAR solicitud peritacion][NoLink]
- [CREAR resultado peritacion][NoLink]
- [MODIFICAR resultado peritacion][NoLink]

#### **61 Crear Modificar Detalle de daños**  
Crear si no existe o Modificar el detalle de los daños de la peritación, por lo que la [operaciones][Operacion] que se pueden ejecutar son:

- [CREAR Detalle de daños][NoLink] 
- [MODIFICAR  peritación][NoLink].  

#### **62 Crear Órdenes de Reparación**  
Genera una orden de reparación si no existe y si existe la modifica, por lo que las [operaciones][Operacion] que se ejecutan son:

- [CREAR orden reparación ][NoLink] 
- [MODIFICAR orden reparación][NoLink].  

#### **70 Entrada y Salida de un inventario en Salvamentos**
Genera la entrada de un inventario y si ya está registrado, genera la salida del inventario , por lo que las [operaciones][Operacion] que se pueden ejecutar son:

-  [CREAR entrada inventario][NoLink]
-  [CREAR salida inventario][NoLink]

#### **71 Actualización del Inventario en Salvamentos**  
Genera la información del inventario y si ya está registrado, o genera la actualización del inventario si ya existe. Este proceso puede generar distintas [operaciones][Operacion]:

- [CREAR salvamento][NoLink] 
- [MODIFICAR salvamento][NoLink].  

#### **72 Crear y Modificar Subastas**  
Crear si no existe o Modificar si existe, una subasta. Este proceso puede generar distintas [operaciones][Operacion]:

- [CREAR Subasta][NoLink] 
- [MODIFICAR Subasta][NoLink]

#### **73 Selección de Inventarios a Subasta y Asociación de Expedientes a Inventarios**  
Asocia un siniestro o expediente a una inventario y un inventario a una subasta. Este proceso puede generar distintas [operaciones][Operacion]: 

- [ASOCIAR siniestro salvamento][NoLink]
- [ASOCIAR expediente salvamento][NoLink]
- [ASOCIAR inventario subasta][NoLink]

#### **74 Anulación de inventario**  
Anula un inventario de salvamentos, por lo que la [operación][Operacion] que se ejecuta es [ANULAR inventario][NoLink].  

#### **75 Anulación Salvamento**  
Actualiza la subasta anulando un inventario que no ha podido venderse y que no se va a poder vender, por lo que la [operación][Operacion] que se ejecuta es [ANULAR inventario][NoLink].  

#### **76 Liberación Salvamento**  
Actualiza una subasta, liberando un inventario y dejando pendiente dicho inventario para poder ser asociado a otra subasta, por lo que la [operación][Operacion] que se ejecuta es [LIBERAR inventario][NoLink].  

#### **77 Venta del Inventario**  
Actualiza una subasta, actualizando el  inventario como vendido actualizando los datos de la venta [operación][Operacion] que se ejecuta es [VENDER inventario][NoLink].  

#### **80 Siniestros judiciales**    
Crear si no existe o Modificar si existe, los datos de la demanda de un juicio. Este proceso puede generar distintas [operaciones][Operacion]: 

- [CREAR juicio demanda][Nolink]
- [MODIFICAR juicio demanda][Nolink]
- [ASOCIAR juicio expediente][Nolink] 
- [CREAR juicio intervención ][NoLink]
- [MODIFICAR juicio intervención ][NoLink]

#### **81 Crear Datos de la Sentencia**  
Crear si no existe o Modificar si existe, los datos de la sentencia de un juicio. Este proceso puede generar distintas [operaciones][Operacion]:

- [CREAR juicio sentencia][Nolink]
- [MODIFICAR juicio sentencia][Nolink]
- [ASOCIAR juicio expediente][Nolink]
- [CREAR juicio intervención][NoLink]
- [MODIFICAR juicio intervención][NoLink]


#### **110 Crear Fraude Siniestro**    
Genera un nuevo Fraude para un siniestro, por lo que la [operación][Operacion] que se ejecuta es [CREAR fraude][NoLink].
  
#### **111 Modificar Fraude sinestro**    
Genera una modificación a un Fraude de un siniestro, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR fraude][NoLink]. 

#### **112 Crear Fraude Expediente**  
Genera un nuevo Fraude para un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR fraude expediente][NoLink].

#### **114 Modificar Fraude Expediente**  
Genera una modificación a un Fraude de un expediente, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR fraude expediente][NoLink].   
 
#### **115 Crear I.Q.R.F. Siniestro**     
Genera una modificación a un I.Q.R.F. de un siniestro, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR i.q.r.f.][NoLink]. 

#### **116 Modificar I.Q.R.F.  Siniestro**  
Genera una modificación a un I.Q.R.F. de un siniestro, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR i.q.r.f.][NoLink].  

#### **117 Crear I.Q.R.F.  Expediente**   
Genera un nuevo I.Q.R.F. para un expediente, por lo que la [operación][Operacion] que se ejecuta es [CREAR i.q.r.f expediente][NoLink].  

#### **118 Modificar I.Q.R.F. Expediente**  
Genera una modificación a un I.Q.R.F. de un expediente, por lo que la [operación][Operacion] que se ejecuta es [MODIFICAR i.q.r.f. expediente][NoLink].  

### **Fecha**
Fecha del Proceso Masivo.

## **Propiedades adicionales a la operación** {#propiedadesadicionales}
### **Orden**
El sistema permite crear más de un proceso masivo en una misma fecha. Esta propiedad es la que diferencia un proceso de otro en un mismo día. 

### **Alias**
Permite crear una descripción que haga que el proceso masivo definido contenga información concreta. 

Por ejemplo, si se define un proceso masivo que abran los siniestros desde otra aplicación del mes de agosto, se puede especificar esta propiedad con esta información (Aperturas Centro Telefónico de agosto), número de orden 1, número de orden 2.

### **Situación del Proceso**
Indica en que estado se encuentra el proceso. Cuando estamos creando un proceso masivo el proceso debe contener un '1', que indica que no se ha procesado.



[LogicaDeNegocio]:  <../../../../../../99-Terminos/TRON-Terminos.md#logicadenegocio>
[Operacion]:        <../../../../../../99-Terminos/TRON-Terminos.md#operacion>


[Tecnica]: <./CREAR-Proceso-masivo-siniestros-TECNICA.md>

[DEFINICIÓN de proceso masivo de Emisión]: <>

[ALTERAR aplicación]: <>

[NoLink]: <>