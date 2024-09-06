![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# Relación entre Oficinas Gestoras y Tramitadoras {#titulo}

==EN CONSTRUCCIÓN==  

## **Objetivo** 
La finalidad es definir por sector para cada oficina comercial (nivel3 de la estructura comercial) que pueda emitir pólizas, cual va a ser la oficina tramitadora que se encargue de gestionar sus expedientes. Dentro de cada oficina tramitadora, existirá un pull de tramitadores especializados para poder asignar el expediente a uno de ellos, según los parámetros establecidos, especialización, carga de trabajo, etc.

## **Propiedades**

### **Sector**
Esta propiedad contendrá el __[la clave del sector][sector]__ para el que vamos a asignar a cada oficina gestora, su tramitadora.

Se podrá utilizar el sector *Genérico 9999*, que significará que la definición que se está realizando es para todos los sectores.

[sector]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-de-Sector.md#titulo>

### **Comercial**
Esta propiedad contendrá la oficina comercial, gestora, a la que le estamos asignando una oficina tramitadora. Estas deberán existir como __[Nivel3][nivel3]__ de la estructura comercial.


[nivel3]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/02-Estructura-Comercial/DEFINICION-Nivel3-Estructura-Comercial.md#titulo>

### **Tramitadora**
Esta propiedad contendrá la oficina tramitadora encargada de gestionar los expedientes de las pólizas que pertenezcan a la oficina comercial. Estas deberán existir en la definición de __[tramitadoras][tramitadora]__.

[tramitadora]:<../108-Estructura-Tramitadora/DEFINIR-Oficinas-Tramitadoras.md#titulo>

Ejemplos:
 
- Se quiere definir  para el **sector 3 Autos**, todos los siniestros que  se abran desde el CALL CENTER, cuya póliza pertenezca a la comercial (cod_nivel3) 1001, se tramite en  la tramitadora 1001.   

  |Ramo|Gestora|Tramitadora|
  |---|---|---|
  |3 (Autos) | 1001 (Madrid Centro)|1001 Madrid Centro

- Se quiere definir  para el **sector 3 Autos**, todos los siniestros que se abran desde el CALL CENTER, cuya póliza pertenezca a la comercial (cod_nivel3) 1002, se tramite en  la tramitadora 1001.

   |Ramo|Gestora|Tramitadora|
  |---|---|---|
  |3 (Autos) | 1002 (Madrid Centro)|1001 Madrid Centro

- Se quiere definir  para **todos los sectores***, todos los siniestros que se abran desde CALL CENTER, cuya póliza pertenezca a la comercial (cod_nivel3) 1003, se tramite en  la tramitadora 1000.

  |Ramo|Gestora|Tramitadora|
  |---|---|---|
  |999 (Autos) | 1003 (Madrid Sur)|1000 Central
 

## Preguntas frecuentes
- ¿Para se utiliza esta definición  ?
    Esta definición se suele utilizar como apoyo para la asignación de un siniestro o expediente a los  tramitadores o supervisores.
    Cuando el siniestro se abre desde un CALL CENTER, se suele acceder a esta definición para ver que tramitadora le corresponde a la comercial de la póliza, o que tramitadora le corresponde a la gestora donde se ha producido el siniestro.
- ¿Es obligatorio introducir datos en esta definición?  
  Eso va a depender de los criterios de asignación que se utilice en la compañía.
  

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>

