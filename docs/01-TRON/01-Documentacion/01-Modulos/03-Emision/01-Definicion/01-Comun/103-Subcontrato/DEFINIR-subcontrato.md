![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# DEFINICIÓN de subcontrato {#titulo}

## **Objetivo**
Bajo este concepto se permite realizar alteraciones de un ramo y un contrato ya definido. Estas alteraciones afectan a un número de conceptos de negocio (no a todos). A continuación se muestra un ejemplo:

Se parte de la definición de un ramo en que las coberturas se encuentran de la siguiente forma:

| RAMO            | CONTRATO    | SUBCONTRATO |
| :---            | :---        | :---        |
| 300 - Automóvil | NO DEFINIDO | NO DEFINIDO |

######

| COBERTURA                 | INHABILITADA |
| :---                      | :---:        |
| 100 Responsabilidad civil | NO           |
| 200 Daños propios         | NO           |
| 300 Accidentes            | SI           |
| 400 Muerte                | NO           |

Para el ramo del ejemplo se define un contrato (SANTANDER) donde se modifica las definición de coberturas:

| RAMO            | CONTRATO  | SUBCONTRATO |
| :---            | :---      | :---        |
| 300 - Automóvil | SANTANDER | NO DEFINIDO |

######

| COBERTURA                 | INHABILITADA |
| :---                      | :---:        |
| 100 Responsabilidad civil | NO           |
| 200 Daños propios         | NO           |
| 300 Accidentes            | NO           |
| 400 Muerte                | NO           |

Bajo el contrato SANTANDER se define un subcontrato (ASEGURADO CON SEGURO DE VIDA):

| RAMO            | CONTRATO  | SUBCONTRATO                  |
| :---            | :---      | :---                         |
| 300 - Automóvil | SANTANDER | ASEGURADO CON SEGURO DE VIDA |

######

| COBERTURA                 | INHABILITADA |
| :---                      | :---:        |
| 100 Responsabilidad civil | NO           |
| 200 Daños propios         | NO           |
| 300 Accidentes            | NO           |
| 400 Muerte                | SI           |

En este ejemplo, cuando se emite una nueva póliza SIN contrato, la cobertura de Muerte SI se ofrece. Cuando se emite una nueva póliza con el contrato SANTANDER SIN subcontrato, la cobertura de Vida SI se ofrece. En cambio, si se emite una póliza del contrato SANTANDER, subcontrato ASEGURADO CON SEGURO DE VIDA, la cobertura de Muerte NO se ofrece.

## **Propiedades**
### **Contrato**
Clave por el que se identificará.

### **Nombre**
Descripción por el que se identificará.

### **Nombre corto**
Descripción corta por el que se identificará.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)
