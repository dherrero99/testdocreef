![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# DEFINICIÓN de contrato {#titulo}

## **Objetivo**
Bajo este concepto se permite realizar alteraciones de un ramo ya definido. Estas alteraciones afectan a un número de conceptos de negocio (no a todos). A continuación se muestra un ejemplo:

Uno de los conceptos de negocio que se define en un ramo son las coberturas. En la definición se establece cuales se van a ofrecer o ya no se ofrecen más. A continuación (como ejemplo), se muestra las coberturas de un ramo y su estado (habilitada o inhabilitada):

| RAMO            | CONTRATO     |
| :---            | :---         |
| 300 - Automóvil | SIN CONTRATO |

######

| COBERTURA                 | INHABILITADA |
| :---                      | :---:        |
| 100 Responsabilidad civil | NO           |
| 200 Daños propios         | NO           |
| 300 Accidentes            | SI           |

Como se puede observar, la cobertura Accidentes se encuentra inhabilitada lo que quiere decir que NO se ofrece en la emisión de una nueva póliza.   
Cuando se hace referencia a que un contrato permite alterar los conceptos de negocio definidos y, atendiendo a este ejemplo, es posible que un contrato SI ofrezca la cobertura de Accidentes aunque el ramo NO la ofrezca. En este ejemplo, se muestra la definición de las coberturas para un contrato:

| RAMO            | CONTRATO  |
| :---            | :---      |
| 300 - Automóvil | SANTANDER |

######

| COBERTURA                 | INHABILITADA |
| :---                      | :---:        |
| 100 Responsabilidad civil | NO           |
| 200 Daños propios         | NO           |
| 300 Accidentes            | NO           |

El resumen de la definición sería:

| RAMO            |
| :---            |
| 300 - Automóvil |
   
######   

| COBERTURA                 | INHABILITADA (SIN CONTRATO) | INHABILITADA (CONTRATO SANTANDER) |
| :---                      | :---:        | :---:              |
| 100 Responsabilidad civil | NO           | NO                 |
| 200 Daños propios         | NO           | NO                 |
| 300 Accidentes            | SI           | NO                 |

En este ejemplo, cuando se emite una nueva póliza SIN contrato, la cobertura de Accidentes NO se ofrece. En cambio, cuando se emite una nueva póliza con el contrato SANTANDER, la cobertura de Accidentes SI se ofrece.

## **Propiedades**
### **Contrato**
Clave por el que se identificará.
### **Nombre**
Descripción por el que se identificará.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)


