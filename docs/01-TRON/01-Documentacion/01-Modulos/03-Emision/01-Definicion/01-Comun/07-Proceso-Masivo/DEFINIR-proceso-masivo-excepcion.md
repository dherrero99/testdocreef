![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# DEFINICIÓN de Excepciones

## **Objetivo**
Detallar causas por las que un [elemento][elemento] candidato en un proceso masivo quedaría fuera del proceso. Es decir, el [elemento][elemento] no será procesado.
Un ejemplo podría ser una póliza que llega a su vencimiento y NO debe renovarse. Esta póliza pasa al proceso de renovación como candidata, pero el cliente decide no renovar la póliza. Para que la póliza no sea procesada (renovada en el ejemplo), debe excepcionarse. En este caso, podría existir una excepción cuya descripción podría ser: "NO RENOVADA POR PETICIÓN DEL CLIENTE".

## **ATRIBUTOS**
### **Excepción**
Toda excepción debe contener una clave única, la cual actúa como identificador de esta.

### **Nombre de la excepción**
Descripción que identificará la excepción. Sirva como ejemplo el visto anteriormente cuando el cliente no desea renovar su póliza.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[Elemento]: <../../../../../../99-Terminos/TRON-Terminos.md#elemento>

