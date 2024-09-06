![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: Completar y revisar descripción de los distintos pasos, visión técnica y links**)

# DESCONTAR comisión en el cobro de recibo ([enlace con visión técnica][Tecnica]) {#titulo} 

## **¿En qué consiste?**
Cada instalación podrá decidir si permite que un agente se descuente la comisión, correspondiente al [recibo][recibo], en el momento del cobro. En este caso, el agente descuenta directamente la comisión, neta de retención, del importe entregado por el cliente, considerándose este movimiento como un anticipo de comisión.

Solamente podrá descontarse la comisión el agente principal de la póliza, siempre que sea el [gestor de cobro][gestor-cobro] del [recibo][recibo].

## **Objetivo**
Registrar el cobro de la comisión, por parte del agente de la póliza, de forma anticipada.

## **Proceso a seguir**
El proceso comprende los siguientes pasos que se hacen de forma automática:

### Insertar [registro diario][registro-diario]
Se realiza un apunte en el [registro diario][registro-diario], identificando el movimiento como comisión anticipada (PC), el importe de la comisión que se registra es neto de retenciones e impuestos.

Este apunte se generará como un nuevo movimiento en el asiento contable que esté abierto, en la cuenta de descuento de comisiones, imputado de forma contraria al movimiento al movimiento de cobro en el que se realiza el descuento, es decir, en el Debe (D) cuando la comisión se descuenta del cobro de un [recibo][recibo] positivo, o en el Haber (H) cuando se trata de una devolución de prima.

Los importes se registran siempre en la moneda del [recibo][recibo].

### Registrar comisiones como anticipo
La comisión descontada se refleja como un anticipo de comisión, identificado como tipo de devolución vencimiento (2), que refleja que este importe se está descontando en el momento del cobro y no como un anticipo real, y tipo de anticipo, montos (3) que indica que es un importe y no se ha calculado por un porcentaje. De esta forma, en la liquidación de comisiones del agente, se tendrá en cuenta este importe para descontarlo de la liquidación.

### Identificar descuento de comisión en [recibo][recibo]
En este movimiento, se actualiza la información del [recibo][recibo] para dejar reflejado que la comisión ya ha sido descontada. 

[Tecnica]: <./DESCONTAR-Comision-recibo-TECNICA.md>
[gestor-cobro]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/05-Tesoreria/01-Definicion/01-Comun/DEFINICION-Gestor-cobro.md>
[recibo]: <../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#recibo-recibo>
[registro-diario]: <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-tesoreria.md#registro-diario-registrodiario>
