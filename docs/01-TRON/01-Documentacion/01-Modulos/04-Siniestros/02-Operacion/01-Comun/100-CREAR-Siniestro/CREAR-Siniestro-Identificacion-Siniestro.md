![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

# CREAR siniestro - Identificación del Siniestro {#titulo}

## **¿En que consiste?**
Mostrar la información requerida a nivel de siniestro cuando se realiza la operación que CREAR Siniestro.

## **Objetivo**
Conocer que información puede solicitarse en este nivel dependiendo de la [definición][DefinicionRamo] del ramo.

## **Proceso a seguir**
A continuación detallan las propiedades que pueden participar en esta operación

## **Identificación del siniestro** {#InformacionGeneral}
### **Fecha de ocurrencia**
Indica la fecha en la que se produjo el siniestro. Esta fecha no puede ser superior a la del día, excepto que la definición del [ramo][OcurrenciaFuturo] se especifique lo contrario.  

### **Hora de ocurrencia** 
Indica la hora en la que se produjo el siniestro.   
 Si en el la definición del [ramo][Horaobligatoriaemision]  la fecha de efecto de la póliza la hora y minutos es obligatoria, en la apertura del siniestro será obligatorio introducir hora y minutos de ocurrencia.

### **Fecha de Notificación**
Indica la fecha en la que siniestro ha sido notificado a la empresa.  
Esta fecha puede tomar un [valor inicial][Valorinicialsiniestro], si así se ha definido en el ramo.
Cuando se introduzca la fecha de notificación, se validarará que no sea superior a la del día. Si el ramo tiene definido que se valide la extemporaneidad, realizará dicha validación con los días fijados

### **Hora de Notificación**



[DefinicionRamo]:         <>
[Moneda]:                 <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/01-Moneda/DEFINICION-de-Moneda.md#titulo>
[Horaobligatoriaemision]: <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#registrar-horaminutos>
[OcurrenciaFuturo]:       <../../../../../../../01-TRON/01-Documentacion/01-Modulos/04-Siniestros/01-Definicion/01-Comunes/DEFINIR-Caracteristicas-Siniestros.md#permiteabrirsiniestrosafuturo>

[Valorinicialsiniestro]:  <../../../../../../../01-TRON/01-Documentacion/01-Modulos/04-Siniestros/01-Definicion/01-Comunes/DEFINIR-Valores-Iniciales-Siniestros.md#valorinicialFechanotificacion>


[Nolink]:           <>