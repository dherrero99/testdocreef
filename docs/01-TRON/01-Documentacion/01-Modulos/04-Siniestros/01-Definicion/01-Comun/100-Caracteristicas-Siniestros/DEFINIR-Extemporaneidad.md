![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Extemporaneidad {#titulo} 

<mark>Falta:</mark> Preguntas y respuestas, Link a documentos sin hacer, Revisar las lógicas  
==EN CONSTRUCCIÓN==  

## __Objetivo__
La finalidad es definir para todos los ramos, el tiempo máximo que puede transcurrir entre la fecha de ocurrencia del siniestro y la fecha de notificación o denuncia de este, a la compañía.

## Propiedades por Ramo
En este apartado se detallarán todos los __atributos específicos por ramo__.

### **Sector**
Este atributo indica __[la clave del Sector][sector]__ para el que se va a definir el número máximo de días que puede transcurrir entre la fecha de ocurrencia y la fecha de denuncia del siniestro.

[sector]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-de-Sector.md#titulo>

### **Ramo**
Este atributo indica __[la clave del Ramo][ramo]__ para el que se va a definir el número máximo de días que puede transcurrir entre la fecha de ocurrencia y la fecha de denuncia del siniestro.  
Este atributo permite introducir la clave genérica, que en este caso significaría para todos los ramos del sector.

[ramo]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>

### **Número Máximo de días**
Este atributo indica el número máximo de días que puede transcurrir entre la __fecha de ocurrencia__ y la __fecha de denuncia__ o notificación a la compañía. Si el número de días entre ambas fechas es superior al indicado en este atributo, el siniestro se considerará extemporáneo, es decir fuera de plazo.

Hay un [parámetro a nivel de ramo][extemporaneidad], que indica si se valida la extemporaneidad o no. 

[extemporaneidad]: <./DEFINIR-Caracteristicas-Siniestros.md#valida-extemporaneidad>
 
## Preguntas frecuentes

- ¿Es obligatorio controlar la extemporaneidad?  

    __No es obligatorio__.Hay una lógica a nivel de Ramo dónde se puede determinar si se controla o no. 

Ver vínculo.

Ejemplos: 

- Se puede evaluar que para un cliente VIP, no se tenga en cuenta la extemporaneidad
- Se puede indicar que para determinado Ramo no se tenga en cuenta la extemporaneidad, pero se quede retenido el siniestro para ser Autorizado o Rechazado.

[Referencia a los términos]  
El [Elemento] es un ejemplo de alusión a los Términos.
 
[Elemento]: <../../../../../99-Terminos/TRON-Terminos.md#elemento>
