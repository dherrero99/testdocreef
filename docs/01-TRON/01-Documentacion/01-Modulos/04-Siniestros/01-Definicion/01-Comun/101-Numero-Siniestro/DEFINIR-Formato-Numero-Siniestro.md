![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Formato del Número de Siniestro {#titulo} 

<mark>Falta:</mark> Preguntas y respuestas, Link a documentos sin hacer, Revisar las lógicas
==EN CONSTRUCCIÓN==  

## __Objetivo__

La finalidad es la definición del formato y longitud que va a tener el Número de Siniestro.   
El Número de siniestro es único por compañía.  
La definición no puede cambiarse una vez que se ha abierto un siniestro.  
La longitud del número de siniestro puede llegar a tener como máximo 15 posiciones. 


## Propiedades Generales

### **Información que puede formar parte del Número de Siniestro**
Esta propiedad contiene el Nombre de los atributos que pueden formar parte de la numeración de siniestros.
Los candidatos son:

-	Código de Compañía
-	Código de Sector
-	Código de Ramo
-	Código del Tercer Nivel de la Estructura Comercial
-	Año Reserva
-	Consecutivo

### **Secuencia de la información dentro del Número de Siniestro**
Esta propiedad lo que contiene es, si se quiere que cualquiera de los candidatos forme parte de la numeración, en que orden se va a situar dentro del número de Siniestro.

### **Longitud**
Este atributo indica la longitud del atributo candidato a formar parte de la numeración del siniestro. La longitud total, la suma de todas las longitudes de los candidatos, __no puede superar las 15 posiciones__.
Sólo se podrá modificar la Longitud de:
- Año de Reserva (de 2 o de 4 posiciones)
- Secuencial  (hasta completar la longitud que se quiera)

### **Ejemplo 1.  Formación de  Número de Siniestro:**
En este ejemplo, los campos que van a formar parte de la numeración son los que tienen número de Secuencia, y van a colocarse en la secuencia que se indica.  
En el ejemplo la longitud del Año de reserva es de 2 posiciones y la longitud del consecutivo es de 5 posiciones, siendo la longitud final del número de Siniestro de 14 posiciones.

|Compañía|Campo	|Secuencia|	Longitud|
|---|---|:---:|:---:|
|1|COMPAÑÍA|-- |2 |
|1|SECTOR|-- |3|
|1|RAMO| __2__|3|
|1|NIVEL 3| __1__|4|
|1|AÑO RESERVA| __3__|2|
|1|CONSECUTIVO|__4__|5
 | |  | |__14__


__Números de Siniestros que generaría__:

__Nivel 3 + Ramo + Año Reserva + Consecutivo__  

   1001    + 308 + 23 + 0001  

   100130820230001


### **Ejemplo 2.  Formación de  Número de Siniestro:**
En este ejemplo, los campos que van a formar parte de la numeración son los que tienen número de Secuencia, y al formar el número de siniestro van a colocarse en la secuencia que se indica.  
La longitud del Año de reserva es de 4 posiciones y la longitud del consecutivo es de 8 posiciones, siendo la longitud final del número de Siniestro de 15 posiciones.

|Compañía|Campo	|Secuencia|	Longitud|
|---|---|:---:|:---:|
1|COMPAÑÍA|-- |2 |
1|SECTOR|-- |3|
1|RAMO| __1__|3|
1|NIVEL 3|-- |4|
1|AÑO RESERVA| __2__|4|
1|CONSECUTIVO|__4__|8
 | |  | |__15__|

__Números de Siniestros que generaría__:

__Ramo + Año Reserva + Consecutivo__  

   308 + 2023 + 00000001  
   
   308202300000001
## Vínculos
 
## Preguntas frecuentes


[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
