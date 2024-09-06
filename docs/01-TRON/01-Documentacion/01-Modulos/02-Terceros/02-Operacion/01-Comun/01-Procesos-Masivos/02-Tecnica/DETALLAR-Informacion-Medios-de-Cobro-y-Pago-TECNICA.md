![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DETALLAR Información de los Medios de Cobro y Pago en el Movimiento Diferido del Tercero (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| ML_THP_NWT_XX_PCM              | BUZÓN MEDIOS DE PAGO Y COBRO                                                                        |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| BTC_IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| SQN_VAL | S | N.A. | SI | SECUENCIA | 
| CMP_VAL | S | N.A. | SI | COMPAÑÍA | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DEL DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | DOCUMENTO DEL TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD TERCERO | 
| PCM_SQN_VAL | S | N.A. | SI | SECUENCIAL MEDIO DE PAGO Y COBRO | 
| VLD_DAT | S | N.A. | SI | FECHA VALIDEZ | 
| PCM_TYP_VAL | S | N.A. | SI | TIPO MEDIO DE PAGO Y COBRO | 
| PCM_CSS_VAL | S | N.A. | SI | CLASE MEDIO DE PAGO Y COBRO | 
| ENT_TYP_VAL | S | N.A. | SI | TIPO ENTIDAD | 
| CNY_VAL | S | N.A. | SI | ZONA UNO GEOGRÁFICA | 
| HLR_NAM | S | N.A. | SI | TITULAR | 
| PCM_VAL | S | N.A. | SI | VALOR ENCRIPTADO DEL MEDIO DE PAGO Y COBRO | 
| PCM_KEY_VAL | S | N.A. | NO | CLAVE ENCRIPTADO DEL MEDIO DE PAGO Y COBRO | 
| TKN_TYP_VAL | S | N.A. | SI | TIPO DE TOKEN | 
| TKN_VAL | S | N.A. | NO | TOKEN MEDIO COBRO PAGO Y COBRO | 
| MVM_PCM_TYP_VAL | S | N.A. | SI | TIPO MOVIMIENTO | 
| MVM_PCM_USE_TYP_VAL | S | N.A. | SI | TIPO DE USO DEL MOVIMIENTO DE MEDIO DE PAGO Y COBRO | 
| CRN_VAL | S | N.A. | SI | MONEDA | 
| EXP_MNH | S | N.A. | NO | MES VENCIMIENTO | 
| EXP_YER | S | N.A. | NO | AÑO VENCIMIENTO | 
| PCM_CCK | S | N.A. | SI | MEDIO DE PAGO Y COBRO VALIDADO | 
| DFL_PCM | S | N.A. | SI | MEDIO DE PAGO Y COBRO DEFECTO | 
| PCM_FAV | S | N.A. | SI | MEDIO DE PAGO Y COBRO PREFERIDO | 
| DSB_ROW | S | N.A. | SI | FILA DESHABILITADA | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA MODIFICACIÓN | 
| PRC_THD_VAL | S | N.A. | NO | HILO | 
| PRC_STS_VAL | S | N.A. | NO | SITUACIÓN DEL PROCESO | 
| ACN_ORG_VAL | S | N.A. | NO | ACCIÓN ORIGEN | 
| ERR_IDN_VAL | S | N.A. | NO | IDENTIFICADOR INTERNO DEL ERROR | 
| OBS_VAL | S | N.A. | NO | OBSERVACIONES | 
| IDN_THP_VAL | S | N.A. | NO | IDENTIFICADOR TERCERO | 
| BNE_VAL | S | N.A. | NO | ENTIDAD BANCARIA | 
| ECR_DAA | S | N.A. | NO | DATOS ENCRIPTADOS | 
