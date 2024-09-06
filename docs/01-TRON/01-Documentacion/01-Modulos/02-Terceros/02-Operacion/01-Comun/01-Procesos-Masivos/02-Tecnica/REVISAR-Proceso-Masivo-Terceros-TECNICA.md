![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# REVISAR Proceso Masivo de Terceros (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| ML_THP_NWT_XX_TPP_BTC_ERR      | TABLA BUZON ERRORES PROCESOS BATCH TERCEROS                                                         |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| CMP_VAL | S | N.A. | SI | COMPANIA | 
| BTC_IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| POC_DAT | S | N.A. | SI | FECHA DE TRATAMIENTO | 
| POC_ORD_NBR | S | N.A. | SI | NUMERO DE ORDEN DE PROCESO | 
| PRC_THD_VAL | S | N.A. | SI | HILO | 
| BTC_MVM_THP_TYP_VAL | S | N.A. | SI | TIPO DE MOVIMIENTO BATCH | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DEL DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | DOCUMENTO DEL TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD TERCERO | 
| ERR_SQN_VAL | S | N.A. | SI | ERROR DE SECUENCIA | 
| ERR_IDN_VAL | S | N.A. | SI | IDENTIFICADOR INTERNO DEL ERROR | 
| ERR_OBS_VAL | S | N.A. | SI | OBSERVACION ERROR | 
| ERR_PTH_TXT_VAL | S | N.A. | SI | RUTA EN LA QUE SUCEDE EL ERROR | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA MODIFICACION | 