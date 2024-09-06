![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: Revisar descripción de los distintos pasos y links**)

# REGISTRAR recibo cobrado ([enlace con visión técnica][Tecnica]) {#titulo} 

## **¿En qué consiste?**
Se trata de registrar el importe recibido por el cobro del [recibo][recibo] en el [registro diario][registro-diario], además de actualizar el [recibo][recibo] correspondiente para identificar que ha sido cobrado y registrar el importe que se debe pagar como comisión al agente y otras intervenciones de la póliza.  


## **Objetivo**
Realizar los pasos necesarios para registrar el importe cobrado en la contabilidad y dejar constancia de la nueva situación del [recibo][recibo] como cobrado, además de registrar el importe de las comisiones correspondientes por el cobro del [recibo][recibo].

## **Proceso a seguir**
El proceso comprende los siguientes pasos que se hacen de forma automática:

### Insertar [registro diario][registro-diario]
La operación de cobro de [recibo][recibo] registra un apunte en el [registro diario][registro-diario], identificando el movimiento como cobro de [recibo][recibo] (CT) si el importe del [recibo][recibo] es positivo, o como una devolución del prima (DP), cuando el [recibo][recibo] es negativo.

Este apunte se generará como un nuevo movimiento en el asiento contable que esté abierto, a la cuenta de recibos pendientes, imputado en el Haber cuando el [recibo][recibo] sea positivo o en el Debe cuando se trate de una devolución de prima.

Los importes se registran siempre en la moneda del [recibo][recibo]

### Registrar movimiento histórico
Registra el movimiento de cobro del [recibo][recibo] en el registro histórico de movimientos, donde debe quedar reflejado cualquier movimiento que se realice sobre un [recibo][recibo].

### Actualizar situación recibo
Realiza la actualización de la situación del [recibo][recibo] para indicar que ha sido cobrado (CT). Al realizar el cobro de un [recibo][recibo] se actualiza la situación en todas las [cuotas][cuota] que componen el [recibo][recibo] cobrado.

### Registrar comisiones
En el proceso de cobro se registran las comisiones devengadas por el cobro del [recibo][recibo], tanto para el agente como para el resto de intervenciones de la póliza. Esta información servirá de base para el proceso de liquidación de comisiones.

[Tecnica]: <./REGISTRAR-Recibo-cobrado-TECNICA.md>
[recibo]: <../../../../../../../../docs/01-TRON/99-Terminos/TRON-Terminos.md#recibo-recibo>
[cuota]: <../../../../../../../../docs/01-TRON/99-Terminos/TRON-Terminos.md#cuota-cuota>
[registro-diario]: <../../../../../../../../docs/01-TRON/99-Terminos/TRON-Terminos-tesoreria.md#registro-diario-registrodiario>