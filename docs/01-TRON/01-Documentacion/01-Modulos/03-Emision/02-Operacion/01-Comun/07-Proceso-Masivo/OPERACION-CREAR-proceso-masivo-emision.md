![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# CREAR proceso masivo en Emisión {#titulo}

## **¿En que consiste?**
TRON está formado por una serie de [operaciones][Operacion]. Ciertas [operaciones][Operacion] se pueden realizar tanto en el momento (en línea), como diferidas en el tiempo. Cuando una [operación][Operacion] se puede diferir, además, se permite determinar a qué [elementos][Elemento] afectará la [operación][Operacion] (puede ser uno o varios [elementos][Elemento]). Por ejemplo, se puede seleccionar una serie de pólizas a las que realizar un determinado suplemento.

Al proceso que determina qué [operación][Operacion] diferida se va a realizar, a qué [elementos][Elemento] afectará esa [operación][Operacion] y qué modificaciones sufrirán los [elementos][Elemento], se le denomina proceso masivo.

## **Objetivo**
Conocer que acciones se deben realizar para que posteriormente se pueda lanzar una [operación][Operacion] de forma diferida. Este documento no se centra en ninguna [operación][Operacion] en concreto.

## **Proceso a seguir**

``` mermaid
graph LR
  A["CREAR
     movimiento
     diferido (1)"]
  B["SELECCIONAR
     elementos
     candidatos (2)"]
  C{"¿Hay
     excepción?"}
  D["EXCEPCIONAR
     elementos
     candidatos (3)"]
  E{"¿Hay
    que 
    indicar
    cambios?"}
  F["INDICAR cambios
     a elementos
     candidatos (4)"]
  G["FIN"]
  A --> B;
  B --> C;
  C -->|SI| D;
  C -->|NO| E;
  D --> E;
  E -->|SI| F;
  E -->|NO| G;
  F --> G;
  click A "../../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/CREAR-proceso-masivo-emision"
  click B "../../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/SELECCIONAR-Proceso-masivo-elemento-candidato-emision"
  click D "../../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/EXCEPCIONAR-proceso-masivo-elemento-candidato-emision"
  click F "../../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/INDICAR-CAMBIO-proceso-masivo-elemento-candidato-emision"
```
[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

1. [CREAR movimiento diferido](../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/CREAR-proceso-masivo-emision.md)
1. [SELECCIONAR elementos candidatos](../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/SELECCIONAR-Proceso-masivo-elemento-candidato-emision.md)
1. [EXCEPCIONAR elementos candidatos](../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/EXCEPCIONAR-proceso-masivo-elemento-candidato-emision.md)
1. [INDICAR cambios a realizar sobre los elementos candidatos](../../../../../../../01-TRON/01-Documentacion/01-Modulos/03-Emision/02-Operacion/01-Comun/07-Proceso-Masivo/INDICAR-CAMBIO-proceso-masivo-elemento-candidato-emision.md)

[Elemento]:  <../../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#elemento>
[Operacion]: <../../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#operacion>
