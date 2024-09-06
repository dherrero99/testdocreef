![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

# SELECCIONAR siniestros {#titulo}

## **¿En que consiste?**
Determinar qué siniestro/expediente serán candidatos a participar en el proceso masivo que se está definiendo.

## **Objetivo**
Extraer aquellos siniestros/expedientes con los que se pretende realizar la operación que se está definiendo

## **Proceso a seguir**

Para que los [elementos][Elemento] candidatos lleguen al proceso masivo, cada instalación tendrá un proceso personalizado.  
Ejemplos de Procesos de Selección:   

- Proceso para extraer todos aquellos siniestros/expedientes que se abrieron con la reserva promedio y no se ha realizado sobre ellos ningún cambio de valoración. La operación que se estaría definiendo para aplicar sobre estos elementos sería CAMBIAR valoración del Expediente para subir la reserva un 15%.  

- Proceso para extraer todos aquellos siniestros que no tengan expedientes, y que se hayan abierto hace más de 15 años. La operación que se estaría definiendo sería TERMINAR Siniestro sin Expedientes.

- Proceso para volcar los siniestros comunicados en un Centro Telefónico. La operación que se estaría definiendo sería APERTURAR Siniestro.

### Proceso personalizado de la instalación

Cada instalación realizará los procesos de selección de siniestros, expedientes y para ello, debe crear sus propias lógicas que seleccionen los siniestros y expedientes a procesar para crear, para modificar, para crear un juicio, una peritación, una iqrf...

[Elemento]:     <../../../../../../../99-Terminos/TRON-Terminos.md#elemento>
[Operacion]:    <../../../../../../../99-Terminos/TRON-Terminos.md#operacion>
