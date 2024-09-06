![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }


==EN CONSTRUCCIÓN==

# DEFINICIÓN de Plan de Pago

# Objetivo

Conceptualmente un plan de pago establece los distintos criterios que la
entidad aseguradora acuerda con el cliente para la realización de los
pagos de la prima comercial, criterios tales como el número de pagos,
las cuantías asociadas, sus formas de cobro, los avisos de cobro (fecha
de extracción y envío, destinatarios, etc.), las fechas de puesta al
cobro, posibles unificaciones de pagos, etc. estableciéndose una clara
diferenciación entre la primera cuota y las restantes.

Este documento pretende detallar las funcionalidades intrínsecas de TRON
en relación al concepto de fraccionamiento de primas y abordándolas
desde la perspectiva de los procesos de desarrollo de productos y
servicios, emisión-suscripción y gestión de cartera.

Para ello se indicarán las características de los planes de pago y de
las propiedades de las cuotas que los conforman, características y
propiedades cuyas combinaciones como se verá a continuación son lo
suficientemente amplias y flexibles como para permitir que el sistema
pueda fraccionar la prima comercial adaptándose a las necesidades
locales por muy específicas que sean estas.

Todo ello sabiendo que el fraccionamiento de primas no es más que un
sistema utilizado por algunas entidades aseguradoras en determinados
ramos o modalidades de seguro, en virtud del cual se permite al
asegurado que la prima de una anualidad completa, que debería ser
abonada por anticipado y de una sola vez, sea liquidada en varios pagos
periódicos.

En cualquier caso, el fraccionamiento en el pago no supone el
fraccionamiento del seguro, de forma tal que una póliza concertada por
anualidades prorrogables, aunque la liquidación de las primas se efectúe
semestral o trimestralmente, étc. No puede ser libremente rescindida por
el asegurado al finalizar uno de tales periodos sino al vencimiento de
cada anualidad, por lo que la obligación de pagar las primas pendientes
persiste hasta que venza la anualidad completa.

La definición de un Plan de Pago puede o no conllevar la financiación de
la prima del seguro y por ende contemplar el cálculo de intereses por la
financiación realizada, dependiendo de la normativa concreta de la
Legislación Local.

# Propiedades Operativas Comunes

Desde un punto de vista transversal para todas las Direcciones a quienes
va dirigido este documento, las acciones y tareas que se tienen que
contemplar al considerar en TRON la definición de un plan de pago no son
otras que seleccionar sus **características** y definir las
**propiedades** de cada una de sus cuotas.

## Características

La definición de los planes de pago en el sistema se realiza a nivel de
la compañía siendo su comportamiento homogéneo para todos los ramos de
la entidad, si bien y una vez creados podrán ser particularizados para
un cliente o dotarlos con rasgos específicos de acuerdo a las
necesidades y criterios que desde las Direcciones de Negocio necesiten
considerarse.

Los planes de pago en TRON **siempre calculan por
diferencia** el fraccionamiento de la prima de la primera o
la última cuota generada dependiendo de la forma de distribución,
restando al total de la prima de la póliza/suplemento emitido las primas
del resto de cuotas generadas.

### **Número de Cuotas.**

Los planes de pago permiten generar entre 1 y 99 Cuotas y asignar las
propiedades para cada una de ellas de manera individualizada.

^NOTA:^ La generación de las cuotas en TRON, dependiendo del plan de
pago seleccionado en el proceso de emisión-suscripción y de la
definición que se indique específicamente en la creación del [Ramo
Técnico](https://mapfrecorp-my.sharepoint.com/wiki/spaces/CTRON/pages/8714739870864572645),
se realiza, o bien en cada uno de los periodos de 365 días y/o fracción
que conforman la póliza o únicamente en su primer periodo.

Escenario I.- Con fecha 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago de 4 cuotas. Gráficamente el efecto
de dicha definición sería ^(Fig.1)^

![](media/media/image1.tmp){width="4.875in" height="1.125in"}

Escenario II.- Con fecha 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago de 12 cuotas. Gráficamente el efecto
de dicha definición sería ^(Fig.2)^

![](media/media/image2.tmp){width="4.875in" height="1.625in"}

### **Proporcionalidad.**

Esta condición del plan de pago le indica al sistema si el plan de pago
va o no a distribuir la prima comercial y las comisiones calculadas en
la póliza/suplemento de manera proporcional/uniforme de acuerdo al
número de cuotas generadas y al periodo temporal que abarca cada una de
ellas.

### **Forma de generación.**

Esta característica del plan de pago define si la generación de las
cuotas se va a realizar desde una fecha inicial hacia adelante o desde
la fecha de vencimiento de la póliza/suplemento hacia atrás.

Escenario III.- Con fecha 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago de 4 cuotas y con una forma de
generación de las mismas hacia el vencimiento de la póliza. Gráficamente
el efecto de dicha definición sería ^(Fig.3)^

![](media/media/image3.tmp){width="4.875in"
height="1.0833333333333333in"}

Escenario IV.- Con fecha 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago de 4 cuotas y con una forma de
generación de las mismas desde la fecha de vencimiento de la póliza.
Gráficamente el efecto de dicha definición sería ^(Fig.4)^

![](media/media/image4.tmp){width="4.875in"
height="1.2291666666666667in"}

### **Fecha Inicial.**

Si el sentido de la forma de generación del plan de pago es hacia
adelante, el sistema permite ir un paso más allá y definir qué fecha
inicial queremos considerar exactamente para la generación de las
cuotas:

-   La fecha de efecto de la póliza o del suplemento emitido.

-   La fecha que tenga el sistema.

-   La fecha que sea mayor como resultado de la comparación entre la
    fecha que tenga el sistema y la fecha de efecto de la póliza o del
    suplemento emitido.

-   Si ninguna de las opciones anteriores se adecúa a las necesidades de
    la entidad MAPFRE local existe la posibilidad de indicar al sistema
    la fecha inicial, mediante el desarrollo por parte de la Dirección
    de Tecnología local de un *componente software,* a partir de la cual
    se van a generar las cuotas.

En cambio si la forma de generación seleccionada del plan de pago es
hacia atrás, el sistema solamente permite tomar como fecha inicial la
fecha de vencimiento de la póliza o del suplemento emitido.

Escenario V.- Con fecha 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago de 4 cuotas, con una forma de
generación de las mismas hacia el vencimiento de la póliza y cuya fecha
inicial es [la fecha de efecto de la póliza/suplemento
emitido]{.underline}. Gráficamente el efecto de dicha definición sería

![](media/media/image5.tmp){width="4.875in" height="0.96875in"}

 

Escenario VI.- Con fecha de efecto del 01/01/2019 se emite en TRON una
póliza retroactiva de duración anual con un plan de pago de 4 cuotas
cuya forma de generación es hacia el vencimiento de la póliza y cuya
fecha inicial es la [fecha del Sistema]{.underline}. Gráficamente el
efecto de dicha definición sería

![](media/media/image6.tmp){width="4.875in"
height="1.2083333333333333in"}

Escenario VII.- Con fecha de efecto de 01/01/2019 se emite
anticipadamente en TRON una póliza de duración anual, con un plan de
pago de 4 cuotas cuya forma de generación es hacia el vencimiento de la
póliza, y cuya fecha inicial sea [la mayor comparando la fecha del
sistema y la fecha de efecto de la póliza/suplemento]{.underline}.
Gráficamente el efecto de dicha definición sería

![](media/media/image7.tmp){width="4.875in" height="1.09375in"}

Escenario VIII.- Con fecha de Efecto del 01/01/2019 se emite
anticipadamente en TRON una póliza de duración anual, con un plan de
pago de 4 cuotas cuya forma de generación es hacia el vencimiento de la
póliza, y cuya fecha inicial será [la que en tiempo real de ejecución
devuelva el *componente Software* desarrollado]{.underline} *(e.g: el
componente devuelve **07/02/2019**).*

![](media/media/image8.tmp){width="4.875in"
height="1.1666666666666667in"}

Escenario IX.- Con fecha 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago de 4 cuotas definido con una forma de
generación de las mismas desde el vencimiento de la póliza.

Gráficamente el único posible efecto de dicha definición sería

![](media/media/image9.tmp){width="4.875in" height="1.21875in"}

### **Fecha Final.**

Dependiendo de la forma de generación del plan de pago debemos
determinar la fecha final que el Sistema debe considerar para la
generación de las cuotas, siendo los posibles valores:

-   La fecha de vencimiento de la póliza o del suplemento realizado.

-   La fecha de efecto de la póliza o del suplemento emitido.

-   Si ninguna de las opciones anteriores se adecúa a las necesidades de
    la entidad MAPFRE local existe una tercera opción mediante el
    desarrollo por parte de la Dirección de Tecnología de un
    *componente* software que recupere la fecha final y que permita
    poder generarlas de acuerdo a los criterios que fueran definidos por
    las Direcciones de Negocio.

Escenario X.- Con fecha de efecto del 01/01/2019 se emite en TRON una
póliza de duración anual, con un plan de pago de 4 cuotas con una forma
de generación hacia adelante y cuya fecha final sea la fecha de
vencimiento de la póliza. Gráficamente el efecto de dicha definición
sería

![](media/media/image10.tmp){width="4.875in"
height="1.0729166666666667in"}

Escenario XI.- Con fecha de efecto de 01/01/2019 se emite en TRON una
póliza de duración anual, con un plan de pago de 4 cuotas que tiene una
forma de generación hacia atrás y cuya fecha final sea la fecha de
efecto de la póliza. Gráficamente el efecto de dicha definición sería

![](media/media/image11.tmp){width="4.875in" height="1.15625in"}

Escenario XII.- Con fecha de efecto del 01/01/2019 se emite en TRON una
póliza de duración anual, con un plan de pago de 4 cuotas con a) una
forma de generación hacia adelante, b) una fecha inicial que se
corresponderá con la fecha de efecto de la póliza y c) la fecha final
será la que en tiempo real de ejecución devuelva el *componente
software* desarrollado *(e.g: el componente devuelve **07/11/2019**).*

Gráficamente el efecto de dicha definición sería

![](media/media/image12.tmp){width="4.875in" height="1.15625in"}

### **Redistribución.**

Puesto que no todas las pólizas emitidas o los suplementos realizados
sobre las mismas cubren siempre una anualidad completa, otra condición
que se tiene que contemplar en las definiciones de los planes de pago es
indicar al sistema cómo se debe comportar y qué acciones debe ejecutar
si las cuotas generadas sobrepasan o exceden los límites teóricos de las
fechas de efecto o vencimiento del movimiento emitido, teniendo en
cuenta obviamente tanto la forma de generación con la que se van a
generar las cuotas como la fecha final del plan de pago.

En estos casos las opciones con las que cuenta el Sistema son:

-   Distribuir proporcionalmente las primas de las cuotas que sobrepasen
    el efecto/vencimiento del movimiento, entre las cuotas que sí entran
    en el periodo.

-   Añadir la prima de las cuotas generadas y que no entren en el
    efecto/vencimiento del movimiento directamente a las primas de la
    primera cuota generada.

-   Omitir la definición del plan de pago y generar una única cuota
    cuyas fechas de efecto y vencimiento sean las fechas de efecto y
    vencimiento de la póliza/suplemento emitido.

-   Permitir sobrepasar la fecha final del plan de pago, y

-   Si ninguna de las opciones anteriores se adecuara a las necesidades
    de la entidad MAPFRE  existe una última alternativa mediante el
    desarrollo por parte de la Dirección de Tecnología local de un
    *componente* *software* que se encargue de distribuir la prima de
    las cuotas que sobrepasen el efecto/vencimiento del movimiento entre
    las cuotas que sí entran con los criterios que consideren y
    determinen las Direcciones de Negocio.

Con fecha de efecto del 01/01/2019 se emite en TRON una póliza cuyo
vencimiento es el 05/07/2019 con un plan de pago de 4 cuotas para una
prima total que asciende a 2.000 \$MX Pesos Mexicanos M/N y cuya a)
fecha inicial será la fecha de efecto de la póliza/suplemento, b) la
forma de generación será hacia el vencimiento del movimiento y c) el
porcentaje de primas de las cuatro cuotas está definido que sea del 25%.

Escenario XIII.- Si en el plan de pago se ha definido que hay que
distribuir proporcionalmente las primas de las cuotas que sobrepasen el
efecto/vencimiento del movimiento, entre las cuotas que sí entran en el
periodo, su efecto sería

![](media/media/image13.tmp){width="4.875in"
height="1.0833333333333333in"}

Escenario XIV.- Si en el sistema se ha definido que hay que adicionar la
prima de las cuotas generadas que no entren en el efecto/vencimiento del
movimiento directamente a las primas de la primera cuota generada, su
efecto sería

![](media/media/image14.tmp){width="4.875in"
height="1.1354166666666667in"}

Escenario XV.- Si en la redistribución del plan de pago se ha definido
que hay que omitir la definición y generar una única cuota, su efecto
sería

![](media/media/image15.tmp){width="4.875in"
height="1.0416666666666667in"}

Escenario XVI.- Si en el sistema se ha definido que se puede sobrepasar
la fecha final del plan de pago, su efecto sería en cambio

![](media/media/image16.tmp){width="4.875in" height="1.3125in"}

Escenario XVII.- Si en el sistema se ha desarrollado y asignado al plan
de pago un \"*componente software"* que pueda distribuir los porcentajes
de las primas de las cuotas que sobrepasen el efecto/vencimiento del
movimiento de acuerdo a las combinaciones de reglas de Negocio y
criterios que se hayan considerado oportunos contemplar, su efecto sería

(Por convención en este ejemplo, el *componente software* devuelve los
porcentajes del 30% excepto para la primera cuota en el que devuelve el
**40%**)

![](media/media/image17.tmp){width="4.875in" height="1.0in"}

### **Prima Mínima.**

Otra característica que debemos contemplar en la definición de los
planes de pago es especificar cómo se tiene que comportar el sistema si
el fraccionamiento de las primas de las cuotas generadas no alcanzara la
prima mínima que la compañía hubiera podido definir y establecer por
divisa/moneda, siendo las posibles opciones:

-   Obviar este control en el plan de pago.

-   Reducir el número total de cuotas generadas hasta que se cumpla la
    condición de alcanzar la prima mínima o quede finalmente una única
    cuota.

-   Generar una única cuota obviando la definición realizada en el plan
    de pago.

-   Avisar de esta circunstancia mediante un mensaje de error que
    detiene el proceso de emisión-suscripción.

-   Permitir generar cuotas sin tener en consideración la prima mínima
    reduciendo el número de cuotas si alguna de ellas no alcanzara la
    prima mínima definida.

Con fecha de efecto de 01/01/2019 se emite en TRON una póliza de
duración anual, con un plan de pago de 4 cuotas que tiene a) una forma
de generación hacia adelante, b) la fecha final ha de ser la fecha de
vencimiento de la póliza, c) Por convención en este ejemplo, la prima
mínima de las cuotas definida por la entidad asciende a 200 Euros y d)
la prima total de la póliza asciende a 1.000 Euros, siendo el porcentaje
de primas de las cuatro cuotas el 40%, el 25%, el 25% y el 10%.

Escenario XVIII.- Si en el sistema se ha definido que no se tenga en
consideración el control de la prima mínima por cuota, el efecto sería

![](media/media/image18.tmp){width="4.875in"
height="1.4479166666666667in"}

Escenario XIX.- Si en el sistema se ha definido que se tenga que reducir
el número total de cuotas generadas hasta que se cumpla la condición de
alcanzar la prima mínima o quede finalmente una única cuota, el efecto
sería

![](media/media/image19.tmp){width="4.875in"
height="3.1666666666666665in"}

Escenario XX.- Si en el sistema se ha definido que no se tenga en
consideración la parametrización del plan de pago sino que solamente
tenga que generar una única cuota, el efecto en esta ocasión sería

![](media/media/image20.tmp){width="4.875in"
height="2.0416666666666665in"}

Escenario XXI.- Si en el sistema se ha definido que se avise de esta
circunstancia mediante un mensaje de error que detenga el proceso de
emisión-suscripción, el efecto sería mostrar un mensaje

![](media/media/image21.tmp){width="3.5416666666666665in"
height="1.7708333333333333in"}

Escenario XXII.- Si en el sistema se ha definido que se puedan generar
cuotas en todo caso con un importe menor a la prima mínima definida y
caso que alguno de ellos no llegue al importe se reduce el número de
cuotas.

### **Comportamiento en Suplementos de Devolución de Primas.**

Siempre y cuando el resultado de la emisión de un suplemento implique un
extorno o [devolución parcial]{.underline} de primas se tiene que
definir cómo se quiere distribuir el importe del mismo entre las cuotas,
siendo las opciones con las que cuenta el sistema:

-   Generación de las cuotas siguiendo la definición del plan de pago.

-   Anulación completa de las cuotas previamente emitidas mientras el
    Importe negativo del Suplemento así lo permita.

-   Distribuyendo el importe negativo del Suplemento de manera
    proporcional entre las cuotas pendientes de cobro.

Con fecha de efecto del 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago proporcional de 4 cuotas para una
prima total que asciende a 2.442 US\$ cuya a) fecha inicial será la
fecha de efecto de la póliza/suplemento y b) la forma de generación será
hacia el vencimiento del movimiento. Originalmente podríamos representar
la emisión:

![](media/media/image22.tmp){width="4.875in"
height="1.0729166666666667in"}

Escenario XXIII.- Sobre esta póliza y con fecha de efecto 05.01.2019 se
emite un suplemento en TRON cuyo resultado final es un extorno de primas
cuya distribución en las cuotas generadas debe realizarse de acuerdo a
la configuración del Plan de Pago de la Póliza (por convención en este
ejemplo, el suplemento implica una anulación parcial de **-100 US\$**)

Gráficamente, el efecto de dicho Suplemento con el Plan de Pago de la
póliza es

![](media/media/image23.tmp){width="4.875in" height="1.25in"}

Escenario XXIV.- Sobre la póliza inicial y con fecha de efecto
01.01.2019, es decir al efecto de la póliza, se emite un suplemento en
TRON cuyo resultado final es un extorno de primas y cuya distribución
debe realizarse mediante la anulación completa de las cuotas previamente
emitidas y mientras el importe negativo del suplemento así lo permita
(por convención en este escenario las cuatro cuotas originales de la
póliza están pendientes de cobro y el suplemento genera un extorno de
primas que asciende a **-810 US\$**)

Gráficamente, el movimiento quedaría representado como

![](media/media/image24.tmp){width="4.875in" height="1.34375in"}

Escenario XXV.- Con fecha de efecto 01.01.2019, es decir al efecto de la
póliza de ejemplo, se emite un suplemento en TRON cuyo resultado final
es un extorno de primas y cuya distribución debe realizarse de manera
proporcional entre las cuotas pendientes de cobro (por convención en
este escenario las cuatro cuotas originales de la póliza están
pendientes de cobro y el Suplemento genera un extorno de primas que
asciende a **-100 US\$**) Gráficamente

![](media/media/image25.tmp){width="4.875in" height="1.4375in"}

^NOTA:^ En el caso particular de los suplementos de
anulación/cancelación total o de rescate en las pólizas de los ramos de
vida ahorro, TRON obvia el comportamiento definido en el plan de pago y
**siempre** intentará compensar los importes positivos de las cuotas
existentes de la póliza con los importes negativos del suplemento,
minimizando en la medida de lo posible su afectación en los procesos de
administración y finanzas de la entidad (obtención del deudor por
primas, pendientes, antigüedad de la deuda...). Además TRON también
obvia en el proceso de emisión de estos dos tipos de suplementos el
cumplimiento de la definición de la propiedad de la prima mínima por
cuota. Dos ejemplos serían:

Escenario XXVI.- Con fecha de efecto del 01/01/2019 se emite en TRON una
póliza de duración anual / 365 días con un plan de pago proporcional de
4 cuotas para una prima total que asciende a 2.442 US\$. Con fecha de
20/03/2019 se realiza la emisión de un suplemento de cancelación total
[prorrata-temporis]{.underline} sobre dicha póliza -- 286 Días.

Gráficamente el efecto en TronWeb de dicha operativa [pudiendo compensar
recibos]{.underline}, sería

![](media/media/image26.tmp){width="4.875in"
height="2.3333333333333335in"}

Si tras haber realizado la compensación quedara un importe de primas y/o
comisiones restante, estos importes se integrarán en una única cuota
cuya fecha de efecto será la fecha de efecto del suplemento que se está
emitiendo y cuya fecha de vencimiento será o bien la fecha de efecto de
la última cuota que se haya compensado totalmente o si no se hubiera
podido compensar ninguna cuota con la fecha de vencimiento del
suplemento que se está emitiendo.

Escenario XXVII.- Con fecha de efecto del 01/01/2019 se emite en TRON
una póliza de duración anual con un plan de pago proporcional de 4
cuotas para una prima total que asciende a 2.442 US\$. Con fecha de
20/03/2019 se emite un suplemento de cancelación total [a
escala]{.underline} sobre dicha póliza siendo el porcentaje de la escala
a utilizarse del 30% (por convención para poder mostrar su efecto en el
ejemplo).

Gráficamente el efecto en TronWeb de dicha operativa [sin poder
compensar recibos]{.underline}, sería

![](media/media/image27.tmp){width="4.875in" height="2.03125in"}

### **Respetar Fechas en Anulación de Suplementos.**

Si en el proceso de gestión de cartera se está realizando
[específicamente la anulación de un suplemento previamente
emitido]{.underline}, en el sistema se tiene que definir expresamente si
se quiere respetar o no la fecha inicial del suplemento que se va a
anular o por el contrario tenemos que generar las cuotas de acuerdo a
las reglas de formación de la fecha inicial del plan de pago del
suplemento que estamos emitiendo.

Con fecha de efecto del 01/01/2019 se emite en TRON una póliza de
duración anual con un plan de pago proporcional de 4 cuotas para una
prima total que asciende a 2.442 US\$ cuya a) fecha inicial será la
fecha de efecto de la póliza/suplemento y b) la forma de generación será
hacia el vencimiento del movimiento. Gráficamente:

![](media/media/image22.tmp){width="4.875in"
height="1.0729166666666667in"}

Con fecha de efecto 05.01.2019 se emite un suplemento cuyo resultado
final, indistintamente un aumento o disminución de primas, implica la
distribución de sus primas de acuerdo a la configuración del Plan de
Pago de la Póliza. Por convención en este ejemplo, el suplemento implica
una prima adicional total de **100 US\$**. Gráficamente, el efecto de
dicho suplemento con el plan de pago de la póliza sería:

![](media/media/image28.tmp){width="4.875in"
height="1.3229166666666667in"}

Escenario XXVIII.- Si con fecha del 27.02.2019 la compañía decide
cancelar el suplemento emitido [teniendo activada]{.underline} la
condición de respetar las fechas del suplemento que vamos a anular,
gráficamente su efecto sería,

![](media/media/image29.tmp){width="4.875in" height="1.53125in"}

Escenario XXIX.- En cambio, si con fecha del 27.02.2019 la entidad
decide cancelar el suplemento emitido [sin tener activada]{.underline}
en el plan de pago la condición de respetar las fechas del suplemento
que vamos a anular, su efecto sería,

![](media/media/image30.tmp){width="4.875in"
height="1.5729166666666667in"}

# Vínculos

# Preguntas Frecuentes

^(1)^ ¿La definición de proporcionalidad de un plan de pago inhibe
alguna otra característica o propiedades de las cuotas en su
parametrización?

Sí, si un plan de pago tiene activada la característica de
proporcionalidad se inhiben las definiciones que tuviera el plan de pago
tanto en las propiedades de porcentaje de primas y porcentaje de
comisiones de las cuotas, como en la característica de redistribución
del Plan de Pago.

^(2)^ ¿Existe alguna recomendación operativa en la definición de los
planes de pago en TRON?

Se recomienda utilizar en las definiciones de los planes de pago la
forma de generación hacia atrás, de vencimiento a efecto, puesto que de
esta manera se va a poder reutilizar en el sistema la numeración de los
recibos generados lo que implica un menor trabajo para la Dirección de
Administración y Finanzas de la compañía y un ahorro en los gastos de
gestión interna.
