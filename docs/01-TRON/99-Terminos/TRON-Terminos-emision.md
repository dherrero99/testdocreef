# TÉRMINOS (TRON)
## Coeficiente de anulación {#coeficiente-anulacion}
Determina cuanto importe hay que devolver en caso de anulación de póliza. Es utilizado exclusivamente en las anulaciones de póliza y en las bajas de riesgo en el que se haya definido en el [ramo][mca_aplica_at_en_riesgo] que se apliquen las mismas reglas como si fuera una anulación de póliza.

Representa el tiempo del movimiento [^tiempo] que se está realizando dividido con el tiempo último suplemento vigente [^tiempo] que sufrió la póliza, expresado en tanto por uno (1/100). El cálculo depende de como sea la anulación, ya que puede ser a prorrata y a escala

| COEFICIENTE DE ANULACIÓN                                            | ORACLE                                        |
| :---                                                                | :---                                          |
| [**días de vigencia del suplemento actual**](#dias-vigencia) entre [**días de vigencia del suplemento anterior vigente**](#dias-vigencia) redondeado a seis decimales | ROUND([**días de vigencia suplemento actual**](#dias-vigencia) / [**días de vigencia suplemento anterior vigente**](#dias-vigencia), 6) |


## Coeficiente de constitución {#coeficiente-constitucion}
Determina cuanto importe del anualizado (que es la base de la tarifa en TRON) aplica a un [movimiento][tip-emision]. Se halla entre el tiempo de un movimiento [^tiempo] y los días que tiene un año, todo ello redondeado a seis decimales y expresado en tanto por uno (1/100). Es decir:

| COEFICIENTE DE CONSTITUCIÓN                                         | ORACLE                                        |
| :---                                                                | :---                                          |
| [**días de vigencia**](#dias-vigencia) entre [**días año**][mca_365_dias] redondeado a seis decimales | ROUND([**días de vigencia**](#dias-vigencia) / [**días año**][mca_365_dias], 6) |

A continuación se muestran varios ejemplos:

| PARÁMETRO DÍAS AÑO |
| :---:              |
| 365                |

######

|ESCENARIO| EFECTO        | VENCIMIENTO     | DÍAS VIGENCIA  | COEFICIENTE DE CONSTITUCIÓN | OBSERVACIONES                      |
| :---:   | :---          | :---            | :---:          | ---:                        | :---                               |
| 1       | 01 enero 2023 | 01 enero 2024   | 365            | 1,000000                    | Aplica el 100% del importe anual   |
| 2       | 01 enero 2023 | 01 octubre 2023 | 273            | 0,747945                    | Aplica el 74,79% del importe anual |
| 3       | 01 enero 2023 | 01 julio 2023   | 181            | 0,495890                    | Aplica el 49,59% del importe anual |
| 4       | 01 enero 2023 | 01 abril 2023   |  90            | 0,246575                    | Aplica el 24,66% del importe anual |

######

| PARÁMETRO DÍAS AÑO |
| :---:              |
| 360                |

######

|ESCENARIO| EFECTO        | VENCIMIENTO     | DÍAS VIGENCIA  | COEFICIENTE DE CONSTITUCIÓN | OBSERVACIONES                    |
| :---:   | :---          | :---            | :---:          | ---:                        | :---                             |
| 1       | 01 enero 2023 | 01 enero 2024   | 360            | 1,000000                    | Aplica el 100% del importe anual |
| 2       | 01 enero 2023 | 01 octubre 2023 | 270            | 0,750000                    | Aplica el 75% del importe anual  |
| 3       | 01 enero 2023 | 01 julio 2023   | 180            | 0,500000                    | Aplica el 50% del importe anual  |
| 4       | 01 enero 2023 | 01 abril 2023   |  90            | 0,250000                    | Aplica el 25% del importe anual  |

## Días de vigencia {#dias-vigencia}
Corresponde a los días que hay entre el efecto y el vencimiento. La forma de calcularlo depende de la definición del ramo de los días que tiene un [año][mca_365_dias]. Es decir:

|PARÁMETRO DÍAS AÑO| DÍAS DE VIGENCIA                                                    | ORACLE                                                           |
| :---:            | :---                                                                | :---                                                             |
| 360              | Meses entre el vencimiento y el efecto multiplicado por 30 días mes | CEIL(MONTHS_BETWEEN(fecha de vencimiento, fecha de efecto) * 30) |
| 365              | Días entre el vencimiento y el efecto                               | fecha de vencimiento - fecha de efecto                           |

A continuación se muestran varios ejemplos dependiendo del valor del parámetro de días año:

|PARÁMETRO DÍAS AÑO|
| :---:            |
| 365              |

######

| EFECTO        | VENCIMIENTO     | DÍAS DE VIGENCIA |
| :---          | :---            | :---:            |
| 01 enero 2023 | 01 febrero 2023 | 31               |
| 01 enero 2023 | 15 febrero 2023 | 45               |

######

|PARÁMETRO DÍAS AÑO|
| :---:            |
| 360              |

######

| EFECTO        | VENCIMIENTO     | Nº DE MESES      | Nº DÍAS MES | RESULTADO        | DÍAS DE VIGENCIA |
| :---          | :---            | ---:             | :---:       | ---:             | :---:            |
| 01 enero 2023 | 01 febrero 2023 | 1,00             | 30          | 30               | 30               |
| 01 enero 2023 | 15 febrero 2023 | 1,45161290322581 | 30          | 43,5483870967742 | 44               |

## Periodo de vigencia {#periodo-vigencia}
Tiempo entre la emisión inicial (en caso que la póliza sea nueva) o la última renovación (en caso que la póliza haya sufrido ya renovaciones) y el vencimiento.

``` mermaid
graph LR
  A(("Nueva emisión"))
  B(("Vencimiento"))
  A <-- "periodo de vigencia" --> B;
```

``` mermaid
graph LR
  A(("Renovación"))
  B(("Vencimiento"))
  A <-- "periodo de vigencia" --> B;
```

## TEMPORALIDAD DE PÓLIZA
### Anual prorrogable {#anual-prorrogable}
Póliza cuya duración es de un año y cuando llega al vencimiento, pasará a renovarse por otro año.

``` mermaid
graph LR
  A["01 enero 2023"]
  B["01 enero 2024"]
  C["01 enero 2025"]
  D["01 enero ..."]
  A -.-> B;
  B -.-> C;
  C -.-> D;
```

### Temporal no renovable {#temporal}
Póliza que cuando llega al vencimiento, no será renovada y pasará a estar expirada.

``` mermaid
graph LR
  A["01 enero 2023"]
  B["01 enero 2024"]
  A -.-> B;
```

### Temporal renovable por su periodo {temporal-renovable-periodo}
Póliza cuya duración es menor a un año y cuando llega al vencimiento, si se renueva, se renovará por el mismo periodo de tiempo.

Es decir, si una póliza por ejemplo tiene vigencia por el periodo lectivo (en Europa de septiembre a junio), cuando se renueve, se vuelve a renovar por el periodo lectivo.

``` mermaid
graph LR
  A["01 septiembre 2023"]
  B["01 julio 2024"]
  C["01 septiembre 2024"]
  D["01 julio 2025"]
  E["01 septiembre ..."]
  F["01 julio ..."]
  A -.-> B;
  C -.-> D;
  E -.-> F;
```

### Temporal renovable por su temporalidad  {#temporal-renovable-temporalidad}
Póliza cuya duración es menor a un año y cuando llega al vencimiento, si se renueva, se renovará por el mismo tiempo.

Es decir, si una póliza por ejemplo tiene una duración de tres meses, cuando se renueve, se renueva por otros tres meses.

``` mermaid
graph LR
  A["01 enero 2023"]
  B["01 julio 2023"]
  C["01 enero 2024"]
  D["01 julio ..."]
  A -.-> B;
  B -.-> C;
  C -.-> D;
```

### Temporal renovable {#temporal-renovable}
Póliza cuya duración es menor a un año y cuando llega al vencimiento, si se renueva, pasará a ser de un año. A partir de esa primera renovación, la póliza pasará a tener la duración anual prorrogable.

``` mermaid
graph LR
  A["01 enero 2023"]
  B["01 mayo 2023"]
  C["01 mayo 2024"]
  D["01 mayo 2025"]
  E["01 mayo ..."]
  A -.-> B;
  B -.-> C;
  C -.-> D;
  D -.-> E;
```

## TIPOS DE EMISIÓN
### Solicitud {#tip-emision-C}
Este tipo se refiere a la las operaciones:

|OPERACIÓN|
| :---    |
| [COTIZAR póliza][COTIZAR-poliza] |
| [EMITIR presupuesto][EMITIR-presupuesto] |
| [EMITIR presupuesto desde presupuesto][EMITIR-presupuesto-desde-presupuesto] |
| [EMITIR presupuesto desde suspensión][EMITIR-presupuesto-desde-suspension] |
| [EMITIR presupuestos desde póliza][EMITIR-presupuestos-desde-poliza] |

### Póliza {#tip-emision-P}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [EMITIR póliza][EMITIR-poliza] |
| [EMITIR póliza desde presupuesto][EMITIR-poliza-desde-presupuesto] |
| [EMITIR póliza desde suspension][EMITIR-poliza-desde-suspension] |
| [EMITIR póliza multiusuario][EMITIR-poliza-multiusuario] |

### Suplemento {#tip-emision-S}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [ALTERAR póliza][ALTERAR-poliza] |
| [ALTERAR póliza anualidad anterior][ALTERAR-poliza-anualidad-anterior] |
| [ALTERAR póliza cambio agente][ALTERAR-poliza-cambio-agente] |
| [ALTERAR póliza desde suspensión][ALTERAR-poliza-desde-suspension] |
| [ALTERAR póliza plan pago][ALTERAR-poliza-plan-pago] |
| [ALTERAR póliza plan pago temporal][ALTERAR-poliza-plan-pago-temporal] |
| [ALTERAR póliza temporalmente][ALTERAR-poliza-temporalmente] |
| [ANULAR póliza][ANULAR-poliza] |
| [ANULAR póliza extinción riesgo][ANULAR-poliza-extincion-riesgo] |
| [ANULAR póliza modificación][ANULAR-poliza-modificacion] |
| [ANULAR póliza modificación anualidad anterior][ANULAR-poliza-modificacion-anualidad-anterior] |
| [ANULAR póliza modificación temporal][ANULAR-poliza-modificacion-temporal] |
| [DISMINUIR póliza por siniestro][DISMINUIR-poliza-por-siniestro] |
| [EXTENDER póliza vigencia][EXTENDER-poliza-vigencia] |
| [LIQUIDAR póliza][LIQUIDAR-poliza] |
| [PRERENOVAR póliza][PRERENOVAR-poliza] |
| [REGULARIZAR póliza][REGULARIZAR-poliza] |
| [REHABILITAR póliza][REHABILITAR-poliza] |
| [REHABILITAR póliza extensión vigencia][REHABILITAR-poliza-extension-vigencia] |
| [REHABILITAR póliza sin extensión vigencia][REHABILITAR-poliza-sin-extension-vigencia] |
| [RENOVAR póliza][RENOVAR-poliza] |
| [RENOVAR póliza desde prerenovación][RENOVAR-poliza-desde-prerenovacion] |
| [RENOVAR póliza desde suspensión][RENOVAR-poliza-desde-suspension] |
| [RESTITUIR póliza capital][RESTITUIR-poliza-capital] |

### Póliza grupo {#tip-emision-R}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [EMITIR póliza][EMITIR-poliza] |
| [EMITIR póliza desde presupuesto][EMITIR-poliza-desde-presupuesto] |
| [EMITIR póliza desde suspension][EMITIR-poliza-desde-suspension] |
| [EMITIR póliza multiusuario][EMITIR-poliza-multiusuario] |

### Remplazada {#tip-emision-Z}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [REEMPLAZAR póliza][REEMPLAZAR-poliza] |
| [REEMPLAZAR póliza renovando][REEMPLAZAR-poliza-renovando] |

### Aplicaciones {#tip-emision-A}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [EMITIR aplicación][EMITIR-aplicacion] |
| [EMITIR aplicación desde declaración][EMITIR-aplicacion-desde-declaracion] |
| [EMITIR aplicación desde supension][EMITIR-aplicacion-desde-supension] |

### Suplemento aplicación {#tip-emision-U}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [ALTERAR aplicación][ALTERAR-aplicacion] |
| [ALTERAR aplicación cambio agente][ALTERAR-aplicacion-cambio-agente] |
| [ALTERAR aplicacion desde suspensión][ALTERAR-aplicacion-desde-suspension] |
| [ALTERAR aplicación plan pago][ALTERAR-aplicacion-plan-pago] |
| [ALTERAR aplicación plan pago temporal][ALTERAR-aplicacion-plan-pago-temporal] |
| [ALTERAR aplicación temporalmente][ALTERAR-aplicacion-temporalmente] |
| [ANULAR aplicación][ANULAR-aplicacion] |
| [ANULAR aplicación modificación][ANULAR-aplicacion-modificacion] |
| [ANULAR aplicación modificación temporal][ANULAR-aplicacion-modificacion-temporal] |
| [LIQUIDAR aplicación][LIQUIDAR-aplicacion] |
| [REHABILITAR aplicación][REHABILITAR-aplicacion] |

### Declaraciones previas {#tip-emision-D}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [EMITIR declaración][EMITIR-declaracion] |

### Reemplazada renovación {#tip-emision-X}
Este tipo se refiere a las operaciones:

|OPERACIÓN|
| :---    |
| [CONVERTIR RENOVACIÓN (cargas en el sistema, renovando)][CONVERTIR-RENOVACION-cargas-en-el-sistema-renovando] |

## TIPOS DE PÓLIZA DE TRANSPORTES
### Póliza fija {#poliza-fija}
Es una póliza estándar.
### Póliza marco con prima en depósito {#poliza-marco-si-prima-deposito}
Póliza en la que el cliente realiza un pago inicial y cuando llega el vencimiento se regularizará mediante un suplemento.
### Póliza marco sin prima en depósito {#poliza-marco-no-prima-deposito}
Póliza en la que el cliente **NO** realiza un pago inicial y que al final del vencimiento se regularizará mediante un suplemento.

## TIPOS DE REVALORIZACIÓN DE COBERTURA
### No revaloriza {#tip-regulariza-1}
La cobertura ni revalorizará ni depreciará. Es decir, el capital no variará en la renovación.

### Especial {#tip-regulariza-2}
Se especificará de que manera revalorizará.

### Por riesgo {#tip-regulariza-3}
Se determina en el momento de la emisión de la póliza.

## TIP DE SUPLEMENTO
### Indeterminado {#tip-spto-IN}
Suplemento que permite múltiples cambios que pueden hacer que la prima varíe, por lo que no se conoce a priori cual será el tipo de suplemento en la salida
Particularidades de este tipo de suplemento:

- Aplica a la anualidad actual

| ENTRADA | SALIDA      |
| :---:   |  :---       |
| IN      | AD, AP o SM |

### Anulación {#tip-spto-AT}
==EN CONSTRUCCIÓN==

### Rehabilitación {#tip-spto-RE}
==EN CONSTRUCCIÓN==

### Cambio forma pago {#tip-spto-CV}
==EN CONSTRUCCIÓN==

### Cambio de agente {#tip-spto-CA}
==EN CONSTRUCCIÓN==

### Extensión vigencia {#tip-spto-MV}
==EN CONSTRUCCIÓN==

### Renovación {#tip-spto-RF}
==EN CONSTRUCCIÓN==

### Regularización {#tip-spto-RG}
Suplemento que afecta a la anualidad anterior cuya finalidad es la de ajustar la situación de la póliza. Puede ser utilizado en pólizas cuyo capital no es fijo durante todo el [periodo de vigencia](#periodo-vigencia) como pueden ser fábricas en el que la producción no es constante en el tiempo, almacenes donde la mercancía varía, etc.
Particularidades de este tipo de suplemento:

- Aplica a la anualidad anterior
- Es un suplemento temporal
- No se halla importe no consumido

| ENTRADA | SALIDA      |
| :---:   |  :---       |
| RG      | AD, AP o SM |

### Emisión {#tip-spto-XX}
Este tipo representa el movimiento que supone la primera emisión de una póliza. Es decir, toda póliza nueva que se crea en TRON, queda almacenada con este tipo de suplemento.

| ENTRADA   | SALIDA      |
| :---:     |  :---       |
| No aplica | XX          |

### Anticipo {#tip-spto-AN}
==EN CONSTRUCCIÓN==

### Recobro de anticipo {#tip-spto-CN}
==EN CONSTRUCCIÓN==

### Rescate {#tip-spto-RS}
==EN CONSTRUCCIÓN==

### Reducción {#tip-spto-RD}
==EN CONSTRUCCIÓN==

### Rehabilitación póliza reducida {#tip-spto-RR}
==EN CONSTRUCCIÓN==

### Aportaciones extraordinarias {#tip-spto-AE}
==EN CONSTRUCCIÓN==

### Anulación de suplemento {#tip-spto-AS}
==EN CONSTRUCCIÓN==

### Extinción del riesgo {#tip-spto-ER}
==EN CONSTRUCCIÓN==

### Seguro prorrogado (vida) {#tip-spto-PG}
==EN CONSTRUCCIÓN==

### Disminución por siniestro {#tip-spto-DS}
==EN CONSTRUCCIÓN==

### Liquidación de transportes {#tip-spto-LT}
==EN CONSTRUCCIÓN==

### Anulación parcial {#tip-spto-AP}
==EN CONSTRUCCIÓN==

### Restitución de capital {#tip-spto-RC}
==EN CONSTRUCCIÓN==

### Adicional {#tip-spto-AD}
==EN CONSTRUCCIÓN==

### Suplemento anualidad anterior {#tip-spto-SA}
==EN CONSTRUCCIÓN==

### Anulación suplemento anualidad anterior {#tip-spto-AA}
==EN CONSTRUCCIÓN==

### Anulación suplemento temporal {#tip-spto-AX}
==EN CONSTRUCCIÓN==

### Rescate parcial {#tip-spto-RP}
==EN CONSTRUCCIÓN==

### Nominativo {#tip-spto-SM}
Este tipo está pensado como tipo de salida, no como entrada. En todo caso, determina que se hicieron modificaciones que no han afectado ni generado información económica o relativa a las comisiones y por consiguiente tampoco se han generado [cuotas][cuota].

| ENTRADA   | SALIDA      |
| :---:     |  :---       |
| No aplica | SM          |

[^tiempo]: Son los días que hay entre el efecto y el vencimiento.

[mca_365_dias]:             <../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#mca_365_dias>
[mca_aplica_at_en_riesgo]:  <../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#mca_aplica_at_en_riesgo>
[tip-emision]:              <../../01-TRON/99-Terminos/TRON-tipo-emision.md#tip-emision>
[cuota]:                    <../../01-TRON/99-Terminos/TRON-Terminos.md#cuota>

[COTIZAR-poliza]:                                      <>
[EMITIR-presupuesto]:                                  <>
[EMITIR-presupuesto-desde-presupuesto]:                <>
[EMITIR-presupuesto-desde-suspension]:                 <>
[EMITIR-presupuestos-desde-poliza]:                    <>
[EMITIR-poliza]:                                       <>
[EMITIR-poliza-desde-presupuesto]:                     <>
[EMITIR-poliza-desde-suspension]:                      <>
[EMITIR-poliza-multiusuario]:                          <>
[ALTERAR-poliza]:                                      <>
[ALTERAR-poliza-anualidad-anterior]:                   <>
[ALTERAR-poliza-cambio-agente]:                        <>
[ALTERAR-poliza-desde-suspension]:                     <>
[ALTERAR-poliza-plan-pago]:                            <>
[ALTERAR-poliza-plan-pago-temporal]:                   <>
[ALTERAR-poliza-temporalmente]:                        <>
[ANULAR-poliza]:                                       <>
[ANULAR-poliza-extincion-riesgo]:                      <>
[ANULAR-poliza-modificacion]:                          <>
[ANULAR-poliza-modificacion-anualidad-anterior]:       <>
[ANULAR-poliza-modificacion-temporal]:                 <>
[DISMINUIR-poliza-por-siniestro]:                      <>
[EXTENDER-poliza-vigencia]:                            <>
[LIQUIDAR-poliza]:                                     <>
[PRERENOVAR-poliza]:                                   <>
[REGULARIZAR-poliza]:                                  <>
[REHABILITAR-poliza]:                                  <>
[REHABILITAR-poliza-extension-vigencia]:               <>
[REHABILITAR-poliza-sin-extension-vigencia]:           <>
[RENOVAR-poliza]:                                      <>
[RENOVAR-poliza-desde-prerenovacion]:                  <>
[RENOVAR-poliza-desde-suspension]:                     <>
[RESTITUIR-poliza-capital]:                            <>
[REEMPLAZAR-poliza]:                                   <>
[REEMPLAZAR-poliza-renovando]:                         <>
[EMITIR-aplicacion]:                                   <>
[EMITIR-aplicacion-desde-declaracion]:                 <>
[EMITIR-aplicacion-desde-supension]:                   <>
[ALTERAR-aplicacion]:                                  <>
[ALTERAR-aplicacion-cambio-agente]:                    <>
[ALTERAR-aplicacion-desde-suspension]:                 <>
[ALTERAR-aplicacion-plan-pago]:                        <>
[ALTERAR-aplicacion-plan-pago-temporal]:               <>
[ALTERAR-aplicacion-temporalmente]:                    <>
[ANULAR-aplicacion]:                                   <>
[ANULAR-aplicacion-modificacion]:                      <>
[ANULAR-aplicacion-modificacion-temporal]:             <>
[LIQUIDAR-aplicacion]:                                 <>
[REHABILITAR-aplicacion]:                              <>
[EMITIR-declaracion]:                                  <>
[CONVERTIR-RENOVACION-cargas-en-el-sistema-renovando]: <>