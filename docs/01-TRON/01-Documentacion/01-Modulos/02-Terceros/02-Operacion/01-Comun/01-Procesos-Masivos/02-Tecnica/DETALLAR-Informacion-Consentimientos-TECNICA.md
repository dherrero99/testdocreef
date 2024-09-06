![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DETALLAR Información de Consentimientos en el Movimiento Diferido del Tercero (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| ML_THP_NWT_XX_TMN              | TABLA BUZÓN CONSENTIMIENTO DE CLIENTE                                                               |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| BTC_IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| SQN_VAL | S | N.A. | SI | SECUENCIA | 
| CMP_VAL | S | N.A. | SI | COMPAÑÍA | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DEL DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | DOCUMENTO DEL TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD TERCERO | 
| COE_VAL | S | N.A. | SI | CÓDIGO CONSENTIMIENTO | 
| VAL_COE_TYP_VAL | S | N.A. | SI | TIPO CONSENTIMIENTO | 
| VLD_DAT | S | N.A. | SI | FECHA VALIDEZ | 
| PRC_THD_VAL | S | N.A. | NO | HILO | 
| PRC_STS_VAL | S | N.A. | NO | SITUACIÓN DEL PROCESO | 
| FRM_TYP_VAL | S | N.A. | SI | TIPO FORMA OTORGADA | 
| COE_INL_DAT | S | N.A. | SI | FECHA INICIO CONSENTIMIENTO | 
| COE_FNL_DAT | S | N.A. | SI | FECHA FIN CONSENTIMIENTO | 
| DSB_ROW | S | N.A. | SI | FILA DESHABILITADA | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_VAL | S | N.A. | SI | FECHA MODIFICACIÓN | 
| ACN_ORG_VAL | S | N.A. | NO | ACCIÓN ORIGEN | 
| ERR_IDN_VAL | S | N.A. | NO | IDENTIFICADOR INTERNO DEL ERROR | 