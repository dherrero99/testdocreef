![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: Revisar si los valores de las columnas son correctos**)

# REGISTRAR recibo cobrado (visión técnica)

## **Modelo de datos involucrado**
Las tablas que intervienen en esta operación son:  

### A5021600  

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| A5021600                       | REGISTRO DIARIO DE OPERACIONES                                                                      |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| COD_CIA | S | N.A. | SI | COMPANIA | 
| FEC_ASTO | D | Cuando cambia respecto a la situacion anterior | SI | FECHA DE ASIENTO  | 
| NUM_ASTO | D | Cuando cambia respecto a la situacion anterior | SI | NUMERO DE ASIENTO  | 
| NUM_OPER_ASTO | S | Toma valor secuencial | SI | NUMERO DE OPERACION DEL ASIENTO  | 
| COD_NIVEL2_CAPTURA | D | Cuando cambia respecto a la situacion anterior | NO | SEGUNDO NIVEL DE LA ESTRUCTUA COMERCIAL DEL USUARIO QUE CAPTURO EL MOVIMIENTO | 
| COD_NIVEL3_CAPTURA | D | Cuando cambia respecto a la situacion anterior | NO | NIVEL3 DE LA ESTRUCTURA COMERCIAL DEL USUARIO QUE CAPTURO EL MOVIMIENTO | 
| COD_NIVEL1 | D | Cuando cambia respecto a la situacion anterior | NO | NIVEL1 DE LA ESTRUCTURA COMERCIAL | 
| COD_NIVEL2 | D | Cuando cambia respecto a la situacion anterior | NO | NIVEL2 DE LA ESTRUCTURA COMERCIAL | 
| COD_NIVEL3 | D | Cuando cambia respecto a la situacion anterior | SI | NIVEL3 DE LA ESTRUCTURA COMERCIAL | 
| TIP_ACTU | S | Si el recibo es positivo toma el valor CT- Cobro del recibo. Si el recibo es negativo toma el valor DP - Devolucion de prima | SI | TIPO DE ACTUALIZACION | 
| COD_CTA | D | Cuando cambia respecto a la situacion anterior | SI | CUENTA CONTABLE | 
| FEC_VALOR | S | Si se permite cambiar la fecha del tipo de cambio toma la fecha indicada por el usuario. Si no se permite cambiar toma la fecha del asiento de tesoreria | SI | FECHA VALOR | 
| FEC_VCTO | S | N.A. | NO | FECHA DE VENCIMIENTO | 
| NUM_CRUCE | D | Si existe cobro anticipado para el recibo toma el valor del numero de cruce que identifica el cobro anticipado | NO | NUMERO DE CRUCE | 
| NOM_MOVIM | S | Toma la descripcion de la agrupacion contable correspondiente al tipo de actualizacion | SI | DESCRIPCION DEL MOVIMIENTO | 
| NUM_POLIZA | S | N.A. | NO | POLIZA | 
| NUM_SPTO | S | N.A. | NO | NUMERO DE SUPLEMENTO | 
| NUM_RECIBO | S | N.A. | NO | RECIBO | 
| COD_CAUSA_ANU | D | Toma valor cuando es devolucion de prima | NO | CAUSA DE ANULACION | 
| TIP_GESTOR | D | Si se permite cambiar el gestor de cobro en el cobro del recibo toma el nuevo tipo de gestor | NO | TIPO DE GESTOR | 
| COD_GESTOR | D | Si se permite cambiar el gestor de cobro en el cobro del recibo toma el nuevo codigo de gestor | NO | GESTOR DE COBRO | 
| NUM_SINI | N | N.A. | NO | SINIESTRO | 
| NUM_EXP | N | N.A. | NO | NÚMERO DE EXPEDIENTE | 
| NUM_LIQ | N | N.A. | NO | LIQUIDATION NUMBER | 
| MCA_CICOS | N | N.A. | NO | MARCA DE CICOS   | 
| COD_RAMO | S | N.A. | NO | RAMO | 
| COD_SECTOR | S | N.A. | NO | SECTOR | 
| COD_AGT | S | N.A. | NO | AGENTE | 
| IMP_MON_PAIS | D | Si el recibo es en una moneda distinta a la del pais toma el valor del importe del recibo aplicando el tipo de cambio | SI | IMPORTE DEL MOVIMIENTO EN MONEDA DEL PAIS | 
| IMP_MON_EXT | S | Toma el valor del recibo en la moneda original | NO | IMPORTE DEL MOVIMIENTO EN MONEDA EXTRANJERA | 
| COD_MON | S | N.A. | SI | MONEDA | 
| VAL_CAMBIO | S | Toma el valor del tipo de cambio a la fecha del asiento del cobro | NO | VALOR DE CAMBIO DE LAS RESERVAS | 
| TIP_IMP | S | Si es un cobro de un recibo positivo toma el valor H - Haber. Si es una devolucion de prima toma el valor D - Debe | SI | TIPO DE IMPORTE CONTABLE (DEBE / HABER) | 
| NOM_RAZON_SOCIAL | N | N.A. | NO | RAZON SOCIAL | 
| COD_ACT_TERCERO | S | N.A. | NO | ACTIVIDAD DEL TERCERO | 
| TIP_DOCUM | S | N.A. | NO | TIPO DEL DOCUMENTO DEL TERCERO | 
| COD_DOCUM | S | N.A. | NO | DOCUMENTO DEL TERCERO | 
| COD_COMPENSACION | N | N.A. | NO | FORMA EN LA QUE EL TERCERO COBRA O PAGA | 
| NUM_CHEQUE | N | N.A. | NO | NUMERO DE CHEQUE | 
| COD_ENTIDAD | N | N.A. | NO | ENTIDAD BANCARIA | 
| COD_OFICINA | N | N.A. | NO | OFICINA BANCARIA | 
| CTA_CTE | N | N.A. | NO | CODIGO DE CUENTA BANCARIA  | 
| CTA_DC | N | N.A. | NO | DIGITO DE CONTROL DE LA CUENTA CORRIENTE BANCARIA | 
| MCA_PLAZA | N | N.A. | NO | MARCA DE PROPIA PLAZA | 
| NOM_PLAZA | N | N.A. | NO | NOMBRE DE LA PLAZA | 
| TIP_CAJA_BCO | N | N.A. | NO | TIPO DE MOVIMIENTO (CAJA / BANCO U OTROS ) | 
| TIP_CTA_SIMP | N | N.A. | NO | TIPO DE CUENTA SIMPLIFICADA   | 
| COD_CTA_SIMP | N | N.A. | NO | CUENTA SIMPLIFICADA | 
| COD_ENTIDAD_CHEQUE | N | N.A. | NO | CODIGO DE ENTIDAD DEL CHEQUE | 
| COD_CAJERO_TT | N | N.A. | NO | CAJERO QUE VA A RECIBIR EL TRASPASO, SI ES NULL NO SE HA ENVIADO, SI NO ES NULL SE HA ENVIADO Y CON MCA_TRASPASO SE SABE SI ESTA RECIBIDO O NO | 
| COD_CTA_SIMP_TT | N | N.A. | NO | CUENTA SIMPLIFICADA DE TRASPASO.  SI ES NULL ESTA PENDIENTE DE ENVIAR AL BANCO.  | 
| MCA_TRASPASO | N | N.A. | NO | ESTADO DEL TRASPASO (NULL-PENDIENTE DE ENVIAR, ANULADO, ENVIADO, RECIBIDO...)  | 
| FEC_FRA | N | N.A. | NO | FECHA DEL DOCUMENTO | 
| NUM_FRA | N | N.A. | NO | NUMERO DEL DOCUMENTO  | 
| COD_RAMO_CTABLE | N | N.A. | NO | RAMO CONTABLE | 
| TIP_TARJETA | N | N.A. | NO | TIPO DE TARJETA DE CREDITO | 
| COD_TARJETA | N | N.A. | NO | CODIGO DE TARJETA DE CREDITO | 
| NUM_TARJETA | N | N.A. | NO | NUMERO DE LA TARJETA DE CREDITO | 
| COD_ACT_TERCERO_IVA | N | N.A. | NO | ACTIVIDAD DEL TERCERO DEL IVA | 
| TIP_DOCUM_IVA | N | N.A. | NO | TIPO DE DOCUMENTO DEL TERCERO DE IVA | 
| COD_DOCUM_IVA | N | N.A. | NO | DOCUMENTO DEL TERCERO DEL IVA | 
| IMP_BASE_IVA | N | N.A. | NO | IMPORTE BASE DEL IVA | 
| IMP_CUOTA_IVA | N | N.A. | NO | IMPORTE CUOTA DE IVA | 
| COD_CTA_CUOTA | N | N.A. | NO | CUENTA PARA LA CUOTA DEL IVA | 
| IMP_BASE_RETEN | N | N.A. | NO | IMPORTE BASE PARA LA RENTENCION | 
| COD_IMPTO | N | N.A. | NO | CODIGO DE IMPUESTO O DE RETENCION | 
| TIP_CTO | N | N.A. | NO | TIPO DEL CONCEPTO (AGENTES, CV/PV, ETC).   | 
| COD_CTO_COB_PAG | N | N.A. | NO | CONCEPTOS QUE PUEDE COBRAR O PAGAR EL USUARIO   | 
| COD_AGRUP_CTABLE | N | N.A. | NO | AGRUPACION DE CONCEPTOS CONTABLES | 
| TIP_ENTORNO | S | Toma el valor 1 - Entorno de recibos | NO | TIPO DE ENTORNO   | 
| NUM_BLOQUE_TES | S | Toma el valor del numero de bloque de tesoreria del asiento | SI | NUMERO DE TRANSACCION DE TESORERIA | 
| NUM_ORD_PAGO | N | N.A. | NO | NUMERO DE ORDEN DE PAGO | 
| NUM_CLAVE | N | N.A. | NO | CLAVE | 
| TIP_TRASPASO | N | N.A. | NO | TIPO DE TRASPASO (CAJA/BANCO ENTRADA/SALIDA) | 
| COD_CAJERO | D | Cuando cambia respecto a la situacion anterior | SI | CAJERO | 
| FEC_ACTU | D | Cuando cambia respecto a la situacion anterior | SI | FECHA DE ACTUALIZACION DE LA FILA | 
| TIP_COBRO | S | Toma el valor 3 - Por parte de tesoreria | NO | TIPO DE COBRO (DOMICILIACION, PARTE, VENTANILLA, ETC) | 
| NUM_INFORMATIVO | N | N.A. | NO | NUMERO INFORMATIVO (CODIGO PARA LOS PAGOS DE RENTAS DE VIDA)   | 
| TXT_AUX1 | N | N.A. | NO | CAMPO AUXILIAR 1 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| TXT_AUX2 | N | N.A. | NO | CAMPO AUXILIAR 2 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| TXT_AUX3 | N | N.A. | NO | CAMPO AUXILIAR 3 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| IMP_AUX1 | N | N.A. | NO | IMPORTE AUXILIAR | 
| NUM_ASTO_220 | N | N.A. | NO | NUMERO DE ASIENTO DEFINITIVO EN LA CONTABILIDAD | 
| NUM_APUNTE_220 | N | N.A. | NO | NUMERO DE APUNTE CORRESPONDIENTE EN LA CONTABILIDAD | 
| COD_CIA_IMPUT | S | N.A. | NO | COMPANIA DE IMPUTACION | 
| TXT_AUX1_CO | N | N.A. | NO | PARAMETRO AUXILIAR 1 DE CONTABILIDAD | 
| TXT_AUX2_CO | N | N.A. | NO | PARAMETRO AUXILIAR 2 DE CONTABILIDAD | 
| TXT_AUX3_CO | N | N.A. | NO | PARAMETRO AUXILIAR 3 DE CONTABILIDAD | 
| COD_CTO_PAGO | N | N.A. | NO | CODIGO DE CONCEPTO DE PAGO | 


### A5020301  

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| A5020301                       | MOVIMIENTOS O HISTORICO DE CUOTAS                                                                   |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| COD_CIA | S | N.A. | SI | COMPANIA | 
| NUM_POLIZA | S | N.A. | SI | POLIZA | 
| NUM_SPTO | S | N.A. | SI | NUMERO DE SUPLEMENTO | 
| NUM_APLI | S | N.A. | SI | NUMERO DE APLICACION | 
| NUM_SPTO_APLI | S | N.A. | SI | SUPLEMENTO DE LA APLICACION | 
| NUM_CUOTA | S | N.A. | SI | CUOTA | 
| NUM_RECIBO | S | N.A. | SI | RECIBO | 
| NUM_MVTO | S | Incrementa en 1 el numero del maximo movimiento del recibo | SI | NUMERO DE MOVIMIENTO | 
| MCA_CA | N | N.A. | SI | LA FILA CORRESPONDE A UN CAMBIO DE AGENTE (ANULA LA FILA ORIGINAL) | 
| MCA_CV | N | N.A. | SI | LA FILA CORRESPONDE A UN CAMBIO DE PLAN DE PAGO (ANULA LA FILA ORIGINAL) | 
| FEC_EFEC_RECIBO | S | N.A. | NO | EFECTO DEL RECIBO | 
| FEC_VCTO_RECIBO | S | N.A. | NO | VENCIMIENTO DEL RECIBO | 
| TIP_GESTOR | S | N.A. | SI | TIPO DE GESTOR | 
| COD_GESTOR | S | N.A. | SI | GESTOR DE COBRO | 
| TIP_SITUACION | S | Toma el valor CT - Cobro total | SI | SITUACION | 
| FEC_SITUACION | S | Toma el valor de la fecha del asiento de tesoreria | NO | FECHA DE ORIGEN DE LA SITUACION | 
| TIP_REMESA | S | N.A. | NO | TIPO DE REMESA PARA CONTROL DE SALDOS(0-AMBOS, 1-PRIMAS,2-STROS .... ) | 
| COD_MON | S | N.A. | SI | MONEDA | 
| VAL_CAMBIO | S | Toma el valor del tipo de cambio a la fecha del asiento del cobro | NO | VALOR DE CAMBIO DE LAS RESERVAS | 
| IMP_RECIBO | S | N.A. | SI | TOTAL DEL RECIBO | 
| IMP_NETA | S | N.A. | NO | PRIMA NETA | 
| IMP_RECARGO | S | N.A. | NO | RECARGOS | 
| IMP_IMPTOS | S | N.A. | NO | IMPUESTOS | 
| IMP_BONI | S | N.A. | NO | BONIFICACIONES | 
| IMP_COMIS | S | N.A. | SI | IMPORTE DE LA COMISION | 
| IMP_TOTAL_COMIS | S | N.A. | NO | TOTAL DE LA COMISION DEL RECIBO | 
| TIP_COASEGURO | S | N.A. | NO | TIPO DE COASEGURO | 
| COD_NIVEL3 | S | N.A. | SI | NIVEL3 DE LA ESTRUCTURA COMERCIAL | 
| COD_AGT | S | N.A. | SI | AGENTE | 
| COD_CAUSA_ANU | D | Toma valor cuando es devolución de prima | NO | CAUSA DE ANULACION | 
| NUM_BLOQUE_TES | S | Toma el valor del numero de bloque de tesoreria del asiento | NO | NUMERO DE TRANSACCION DE TESORERIA | 
| NUM_ORD_PAGO | N | N.A. | NO | NUMERO DE ORDEN DE PAGO | 
| TIP_COBRO | S | Toma el valor 3 - Por parte de tesoreria | NO | TIPO DE COBRO (DOMICILIACION, PARTE, VENTANILLA, ETC) | 
| TXT_AUX1 | S | N.A. | NO | CAMPO AUXILIAR 1 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| TXT_AUX2 | S | N.A. | NO | CAMPO AUXILIAR 2 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| FEC_AUX1 | S | Si se permite cambiar la fecha del tipo de cambio toma la fecha indicada por el usuario. Si no se permite cambiar toma la fecha del asiento de tesorería | NO | FECHA REAL DEL COBRO. SI ESTA RELLENA SERA POR UN COBRO NORMAL O POR LA CANCELACION DE LA PRIMA AVISADA | 
| COD_USR | D | Cuando cambia respecto a la situacion anterior | SI | USUARIO QUE ACTUALIZO LA FILA | 
| FEC_ACTU | D | Cuando cambia respecto a la situacion anterior | SI | FECHA DE ACTUALIZACION DE LA FILA | 
| TIP_DOCUM_PAGO | S | N.A. | NO | TIPO DEL DOCUMENTO DE PAGO | 
| COD_DOCUM_PAGO | S | N.A. | NO | DOCUMENTO DEL TERCERO DEL PAGO | 
| IMP_INTERES | S | N.A. | NO | INTERESES | 
| IMP_IMPTOS_INTERES | S | N.A. | NO | IMPUESTOS DE LOS INTERESES | 
| NUM_MVTO_CV | N | N.A. | NO | NUMERO DE MOVIMIENTO EN UN CAMBIO DE PLAN DE PAGO | 
| MCA_DCTO_COMIS | D | Cuando se descuentan comisiones en el cobro | NO | INDICA SI SE DESCUENTA LAS COMISIONES EN EL MOMENTO DEL COBRO DEL RECIBO | 
| FEC_VCTO_PAGO | S | N.A. | NO | FECHA VENCIMIENTO DE PAGO (ULTIMO DIA DE GRACIA) | 
| COD_CIA_COBRO | D | Cuando cambia respecto a la situacion anterior | NO | COMPANIA DEL COBRO | 
| NUM_MVTO_CA | N | N.A. | NO | NUMERO DE SECUENCIA PARA LOS CAMBIOS DE AGENTE (ROMPE LA PK EN LA ANULACIÓN DE RECIBOS A REGENERAR) | 
| MCA_DTO_IMPTO | D | Cuando se descuentan impuestos en el cobro | NO | DESCUENTO IMPUESTO | 
| MCA_DTO_RECARGO | D | Cuando se descuentan recargos en el cobro | NO | DESCUENTO RECARGO | 
| FEC_CTABLE | D | Cuando cambia respecto a la situacion anterior | NO | PARA EL ASIENTO DE EMISION O FECHA DE PAGO | 
| TIP_DOCUM | S | N.A. | NO | TIPO DE DOCUMENTO DEL TERCERO | 
| COD_DOCUM | S | N.A. | NO | DOCUMENTO DEL TERCERO | 


### A2990700  

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| A2990700                       | RECIBOS/CUOTAS DE UNA POLIZA                                                                        |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| COD_CIA | N | N.A | SI | COMPANIA | 
| NUM_POLIZA | N | N.A | SI | POLIZA | 
| NUM_SPTO | N | N.A | SI | NUMERO DE SUPLEMENTO | 
| NUM_APLI | N | N.A | SI | NUMERO DE APLICACION | 
| NUM_SPTO_APLI | N | N.A | SI | SUPLEMENTO DE LA APLICACION | 
| NUM_CUOTA | N | N.A | SI | CUOTA | 
| NUM_RECIBO | N | N.A | SI | RECIBO | 
| TIP_RECIBO | N | N.A | NO | TIPO DE RECIBO (DOMICILIADO, VENTANILLA, ETC) | 
| FEC_EFEC_RECIBO | N | N.A | SI | EFECTO DEL RECIBO | 
| FEC_VCTO_RECIBO | N | N.A | SI | VENCIMIENTO DEL RECIBO | 
| TIP_GESTOR | N | N.A | SI | TIPO DE GESTOR | 
| COD_GESTOR | N | N.A | SI | GESTOR DE COBRO | 
| FEC_EMISION_SPTO | N | N.A | SI | FECHA DE CONTABILIZACION DEL SUPLEMENTO | 
| TIP_SITUACION | S | Toma el valor CT - Cobro total | SI | SITUACION | 
| TIP_REMESA | N | N.A | NO | TIPO DE REMESA PARA CONTROL DE SALDOS(0-AMBOS, 1-PRIMAS,2-STROS .... ) | 
| FEC_REMESA | N | N.A | NO | FECHA DE REMESA | 
| FEC_CTABLE | N | N.A | NO | PARA EL ASIENTO DE EMISION O FECHA DE PAGO | 
| FEC_VALOR | D | Si se cambia la fecha de valor en el cobro de recibo | NO | FECHA VALOR | 
| COD_MON | N | N.A | SI | MONEDA | 
| VAL_CAMBIO | N | N.A | NO | VALOR DE CAMBIO DE LAS RESERVAS | 
| IMP_RECIBO | N | N.A | SI | TOTAL DEL RECIBO | 
| IMP_NETA | N | N.A | SI | PRIMA NETA | 
| IMP_RECARGO | N | N.A | SI | RECARGOS | 
| IMP_IMPTOS | N | N.A | SI | IMPUESTOS | 
| IMP_BONI | N | N.A | SI | BONIFICACIONES | 
| IMP_COMIS | N | N.A | NO | IMPORTE DE LA COMISION | 
| TIP_COASEGURO | N | N.A | SI | TIPO DE COASEGURO | 
| COD_NIVEL3 | N | N.A | NO | NIVEL3 DE LA ESTRUCTURA COMERCIAL | 
| COD_AGT | N | N.A | SI | AGENTE | 
| NUM_IMPRESION | N | N.A | NO | NUMERO DE VECES QUE SE HA IMPRESO  | 
| CTRL_MOROSO | N | N.A | NO | CONTROL DE AVISO DE MOROSOS | 
| TXT_AUX1 | N | N.A | NO | CAMPO AUXILIAR 1 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| TXT_AUX2 | N | N.A | NO | CAMPO AUXILIAR 2 (PARA DATOS ESPECIFICOS DE UNA INSTALACION.  ESTE CAMPO NO SE DEBE USAR EN INSTALACIONES NUEVAS) | 
| FEC_ACTU | D | Cuando cambia respecto a la situacion anterior | NO | FECHA DE ACTUALIZACION DE LA FILA | 
| IMP_TOTAL_COMIS | N | N.A | NO | TOTAL DE LA COMISION DEL RECIBO | 
| MCA_CA | N | N.A | SI | LA FILA CORRESPONDE A UN CAMBIO DE AGENTE (ANULA LA FILA ORIGINAL) | 
| MCA_CV | N | N.A | SI | LA FILA CORRESPONDE A UN CAMBIO DE PLAN DE PAGO (ANULA LA FILA ORIGINAL) | 
| NUM_AVISO | N | N.A | NO | NUMERO DE AVISO | 
| TIP_DOCUM_PAGO | N | N.A | NO | TIPO DEL DOCUMENTO DE PAGO | 
| COD_DOCUM_PAGO | N | N.A | NO | DOCUMENTO DEL TERCERO DEL PAGO | 
| IMP_INTERES | N | N.A | NO | INTERESES | 
| IMP_IMPTOS_INTERES | N | N.A | NO | IMPUESTOS DE LOS INTERESES | 
| NUM_MVTO_CV | N | N.A | NO | NUMERO DE MOVIMIENTO EN UN CAMBIO DE PLAN DE PAGO | 
| MCA_DCTO_COMIS | N | N.A | NO | INDICA SI SE DESCUENTA LAS COMISIONES EN EL MOMENTO DEL COBRO DEL RECIBO | 
| FEC_VCTO_PAGO | N | N.A | NO | FECHA VENCIMIENTO DE PAGO (ULTIMO DIA DE GRACIA) | 
| NUM_MVTO_CA | N | N.A | NO | NUMERO DE SECUENCIA PARA LOS CAMBIOS DE AGENTE (ROMPE LA PK EN LA ANULACIÓN DE RECIBOS A REGENERAR) | 
| MCA_DTO_IMPTO | N | N.A | NO | DESCUENTO IMPUESTO | 
| MCA_DTO_RECARGO | N | N.A | NO | DESCUENTO RECARGO | 
| TIP_DOCUM | N | N.A | NO | TIPO DOCUMENTO PAGADOR | 
| COD_DOCUM | N | N.A | NO | DOCUMENTO PAGADOR | 


### A5020058  
| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| A5020058                       | COMISIONES DE RECIBOS Y AJUSTES                                                                     |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| COD_CIA | S | N.A. | SI | COMPANIA | 
| NUM_RECIBO | S | N.A. | NO | RECIBO | 
| NUM_POLIZA | S | N.A. | NO | POLIZA | 
| NUM_SPTO | S | N.A. | NO | NUMERO DE SUPLEMENTO | 
| NUM_APLI | S | N.A. | NO | NUMERO DE APLICACION | 
| NUM_SPTO_APLI | S | N.A. | NO | SUPLEMENTO DE LA APLICACION | 
| NUM_CUOTA | S | N.A. | NO | CUOTA | 
| TIP_SITUACION | S | Si el recibo es positivo toma el valor CT- Cobro del recibo. Si el recibo es negativo toma el valor DP - Devolucion de prima | NO | SITUACION | 
| COD_NIVEL1 | S | N.A. | NO | NIVEL1 DE LA ESTRUCTURA COMERCIAL | 
| COD_NIVEL2 | S | N.A. | SI | NIVEL2 DE LA ESTRUCTURA COMERCIAL | 
| COD_NIVEL3 | S | N.A. | SI | NIVEL3 DE LA ESTRUCTURA COMERCIAL | 
| COD_SECTOR | S | N.A. | NO | SECTOR | 
| COD_RAMO | S | N.A. | NO | RAMO | 
| TIP_DOCUM | S | Toma el valor del tipo de documento del tomador de la poliza | NO | TIPO DEL DOCUMENTO DEL TERCERO | 
| COD_DOCUM | S | Toma el valor del codigo de documento del tomador de la poliza | NO | DOCUMENTO DEL TERCERO | 
| COD_AGT | D | Toma el valor de la clave del agente padre | NO | AGENTE | 
| TIP_DOCUM_AGT | D | Toma el valor del tipo de documento del agente padre | NO | TIPO DE DOCUMENTO DEL AGENTE  | 
| COD_DOCUM_AGT | D | Toma el valor del código de documento del agente padre | NO | DOCUMENTO DEL AGENTE | 
| TIP_AGT | D | Cuando cambia respecto a la situacion anterior | NO | TIPO DE AGENTE | 
| COD_MVTO | S | Toma el valor DC - Devengo de comisiones | NO | CODIGO DE MOVIMIENTO | 
| COD_AJUSTE | N | N.A. | NO | CODIGO DE AJUSTE  | 
| COD_CTA | S | Toma el valor del número de cuenta contable del agente | NO | CUENTA CONTABLE | 
| COD_RETEN | N | N.A. | NO | CODIGO DEL IMPUESTO DE RETENCION | 
| COD_MON | S | N.A. | SI | MONEDA | 
| VAL_CAMBIO | S | Toma el valor del tipo de cambio a la fecha del asiento del cobro | NO | VALOR DE CAMBIO DE LAS RESERVAS | 
| IMP_RECIBO | S | Toma valor 0 cuando son comisiones por otros conceptos. Toma el valor del importe total del recibo para el resto de comisiones | NO | TOTAL DEL RECIBO | 
| IMP_MVTO | S | Toma el valor de la comisión | NO | IMPORTE DEL MOVIMIENTO | 
| FEC_MVTO | S | Toma el valor de la fecha del asiento de tesoreria | NO | FECHA DEL MOVIMIENTO | 
| FEC_PROCESO | N | N.A. | NO | FECHA DEL PROCESO | 
| VAL_CAMBIO_PROCESO | N | N.A. | NO | TIPO DE CAMBIO EN EL PROCESO | 
| FEC_ASTO_COM | N | N.A. | NO | FECHA DEL ASIENTO DE COMISIONES  | 
| ANIO_MES | S | Toma el valor del mes y año de la fecha del asiento de tesoreria | NO | ANIO/MES | 
| ORG_OPER | N | N.A. | NO | ORIGEN DE LA OPERACION | 
| COD_RAMO_CTABLE | N | N.A. | NO | RAMO CONTABLE | 
| FOR_ACTUACION | S | Toma el valor dependiendo del intermediario: P-Agente principal 1,2 o 3- Agentes secundarios O-Organizador A-asesor | NO | FORMA DE ACTUACION DEL INTERMEDIARIO ("P","O","A")  | 
| NUM_MVTO_301 | S | Toma el número correspondiente al movimiento en la tabla historica de movimientos de recibos | NO | NUMERO DE MOVIMIENTO EN HISTORICO DE RECIBOS | 
| COD_TIP_COMISION | D | Cuando la información que se inserta es de comisiones no estandar | NO | TIPO DE COMISION (COMISIONES EXTERNAS) | 
| IMP_MVTO_RECA | D | Cuando la información que se inserta es de comisiones estandar toma el importe de la comision sobre recargo | NO | IMPORTE DE LAS COMISIONES SOBRE EL RECARGO. | 
| MCA_EXCLUIR | N | N.A. | NO | INDICA SI SE EXCLUYE EL MOVIMIENTO | 
| TXT_MVTO | N | N.A. | NO | DESCRIPCION DEL MOVIMIENTO | 
| COD_HIJO_AGT | S | Toma el valor del código del agente principal | NO | CODIGO DEL AGENTE HIJO | 
| NUM_BLOQUE_TES | S | Toma el valor del numero de bloque de tesoreria del asiento | NO | NUMERO DE TRANSACCION DE TESORERIA | 
| TIP_COMIS_ECO | N | N.A. | NO | AGRUPADOR DE CONCEPTOS ECONOMICOS QUE SE PAGAN COMO COMISION | 
