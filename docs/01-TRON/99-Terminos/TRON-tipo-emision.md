# TIPOS (EMISIÓN)

## TIPO DE DURACIÓN DE PÓLIZA {#tip-duracion}
Determina la duración de la póliza

| TIPO  | DESCRIPCIÓN |
| :---: | :---        |
| 1 | [ANUAL PRORROGABLE](./TRON-Terminos-emision.md#anual-prorrogable) |
| 2 | [TEMPORAL NO RENOVABLE](./TRON-Terminos-emision.md#temporal) |
| 4 | [TEMPORAL RENOVABLE POR SU PERIODO](./TRON-Terminos-emision.md#temporal-renovable-periodo) |
| 5 | [TEMPORAL RENOVABLE POR SU TEMPORALIDAD](./TRON-Terminos-emision.md#temporal-renovable-temporalidad) |
| 6 | [TEMPORAL RENOVABLE](./TRON-Terminos-emision.md#temporal-renovable) |

## TIPO DE EMISIÓN {#tip-emision}
Determina el movimiento que se pretende realizar

| TIPO  | DESCRIPCIÓN |
| :---: | :---        |
| C | [SOLICITUD](./TRON-Terminos-emision.md#tip-emision-C) |
| P | [PÓLIZA](./TRON-Terminos-emision.md#tip-emision-P) |
| S | [SUPLEMENTO](./TRON-Terminos-emision.md#tip-emision-S) |
| R | [PÓLIZA GRUPO](./TRON-Terminos-emision.md#tip-emision-R) |
| Z | [REMPLAZADA](./TRON-Terminos-emision.md#tip-emision-Z) |
| A | [APLICACIONES](./TRON-Terminos-emision.md#tip-emision-A) |
| U | [SUPLEMENTO APLICACIÓN](./TRON-Terminos-emision.md#tip-emision-U) |
| D | [DECLARACIONES PREVIAS](./TRON-Terminos-emision.md#tip-emision-D) |
| X | [REEMPLAZADA RENOVACIÓN](./TRON-Terminos-emision.md#tip-emision-X) |

## TIPO DE REVALORIZACIÓN DE COBERTURA {#tip-regulariza}
Determina la forma en la que la cobertura revalorizará (si revaloriza)

| TIPO  | DESCRIPCIÓN |
| :---: | :---        |
| 1 | [NO REGULARIZA](./TRON-Terminos-emision.md#tip-regulariza-1) |
| 2 | [ESPECIAL](./TRON-Terminos-emision.md#tip-regulariza-2) |
| 3 | [POR RIESGO](./TRON-Terminos-emision.md#tip-regulariza-3) |

## TIPO DE PÓLIZA DE TRANSPORTES {#tip-poliza-tr}
Determina el tipo de póliza que se creará cuando el tratamiento es de transportes

| TIPO  | DESCRIPCIÓN |
| :---: | :---        |
| F | [PÓLIZA FIJA](./TRON-Terminos-emision.md#poliza-fija)                        |
| C | [PÓLIZA MARCO CON PRIMA EN DEPOSITO](./TRON-Terminos-emision.md#poliza-marco-si-prima-deposito) |
| S | [PÓLIZA MARCO SIN PRIMA EN DEPOSITO](./TRON-Terminos-emision.md#poliza-marco-no-prima-deposito) |

## TIPO DE SUPLEMENTO {#tip-spto}
Determina que modificación se pretende realizar a una póliza y también que resultado produjo esa modificación. Es decir, tiene dos facetas:

1. En la entrada de un proceso, determina que se pretende hacer con una póliza, Por ejemplo, renovar, anular, rehabilitar, ...
1. En la salida de un proceso, determina que ocurrió con esa póliza. Por ejemplo, se devolvió parte de la prima, se anuló, se rehabilitó, ...

Por otro lado, existen tipos que son válidos tanto para la entrada como para la salida del proceso. Otros tipos son válidos para la entrada, pero no para la salida del proceso. Y por último, hay tipos que no son válidos para la entrada y si para la salida del proceso. Esto es:

| TIPO | VÁLIDO ENTRADA | VÁLIDO SALIDA |
| :---:| :---:          | :---:         |
| "A"  | SI             | SI            |
| "B"  | SI             | NO            |
| "C"  | NO             | SI            |

Por ejemplo, un suplemento definido de entrada como Anulación total (AT), la salida también es Anulación total (AT).

``` mermaid
graph LR
  A["AT"]
  B["OPERACIÓN"]
  C["AT"]
  A --> B;
  B --> C;
```
En cambio, un suplemento que se define de entrada como indeterminado (IN), cuando finaliza la operación, los cambios efectuados pueden generar salidas del tipo:

- Se cobró prima (AD)
- Se devolvió prima (AP)
- No se afectó a la prima (SM)

``` mermaid
graph LR
  A["IN"]
  B["OPERACIÓN"]
  C["SM"]
  D["AD"]
  E["AP"]
  A --> B;
  B --> C;
  B --> D;
  B --> E;
```

A continuación se detallan los tipos definidos:

| TIPO  | DESCRIPCIÓN |
| :---: | :---        |
| IN | [INDETERMINADO](./TRON-Terminos-emision.md#tip-spto-IN) |
| AT | [ANULACIÓN](./TRON-Terminos-emision.md#tip-spto-AT) |
| RE | [REHABILITACIÓN](./TRON-Terminos-emision.md#tip-spto-RE) |
| CV | [CAMBIO FORMA PAGO](./TRON-Terminos-emision.md#tip-spto-CV) |
| CA | [CAMBIO DE AGENTE](./TRON-Terminos-emision.md#tip-spto-CA) |
| MV | [EXTENSIÓN VIGENCIA](./TRON-Terminos-emision.md#tip-spto-MV) |
| RF | [RENOVACIÓN](./TRON-Terminos-emision.md#tip-spto-RF) |
| RG | [REGULARIZACIÓN](./TRON-Terminos-emision.md#tip-spto-RG) |
| XX | [EMISIÓN](./TRON-Terminos-emision.md#tip-spto-XX) |
| AN | [ANTICIPO](./TRON-Terminos-emision.md#tip-spto-AN) |
| CN | [RECOBRO DE ANTICIPO](./TRON-Terminos-emision.md#tip-spto-CN) |
| RS | [RESCATE](./TRON-Terminos-emision.md#tip-spto-RS) |
| RD | [REDUCCIÓN](./TRON-Terminos-emision.md#tip-spto-RD) |
| RR | [REHABILITACIÓN PÓLIZA REDUCIDA](./TRON-Terminos-emision.md#tip-spto-RR) |
| AE | [APORTACIONES EXTRAORDINARIAS](./TRON-Terminos-emision.md#tip-spto-AE) |
| AS | [ANULACIÓN DE SUPLEMENTO](./TRON-Terminos-emision.md#tip-spto-AS) |
| ER | [EXTINCIÓN DEL RIESGO](./TRON-Terminos-emision.md#tip-spto-ER) |
| PG | [SEGURO PRORROGADO (VIDA)](./TRON-Terminos-emision.md#tip-spto-PG) |
| DS | [DISMINUCIÓN POR SINIESTRO](./TRON-Terminos-emision.md#tip-spto-DS) |
| LT | [LIQUIDACIÓN DE TRANSPORTES](./TRON-Terminos-emision.md#tip-spto-LT) |
| AP | [ANULACIÓN PARCIAL](./TRON-Terminos-emision.md#tip-spto-AP) |
| RC | [RESTITUCIÓN DE CAPITAL](./TRON-Terminos-emision.md#tip-spto-RC) |
| AD | [ADICIONAL](./TRON-Terminos-emision.md#tip-spto-AD) |
| SA | [SUPLEMENTO ANUALIDAD ANTERIOR](./TRON-Terminos-emision.md#tip-spto-SA) |
| AA | [ANULACIÓN SUPLEMENTO ANUALIDAD ANTERIOR](./TRON-Terminos-emision.md#tip-spto-AA) |
| AX | [ANULACIÓN SUPLEMENTO TEMPORAL](./TRON-Terminos-emision.md#tip-spto-AX) |
| RP | [RESCATE PARCIAL](./TRON-Terminos-emision.md#tip-spto-RP) |
| SM | [NOMINATIVO](./TRON-Terminos-emision.md#tip-spto-SM) |
