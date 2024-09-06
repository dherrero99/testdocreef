![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# CREAR MOVIMIENTO DIFERIDO del Proceso Masivo de Terceros (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| ML_THP_NWT_XX_TPP_BTC                       | TABLA CONTROL PROCESOS MASIVOS TERCEROS                                                                               |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| CMP_VAL | S | N.A. | SI | COMPANIA | 
| BTC_IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| POC_DAT | S | N.A. | SI | FECHA DE TRATAMIENTO | 
| POC_ORD_NBR | S | N.A. | SI | NUMERO DE ORDEN DE PROCESO | 
| PRC_THD_VAL | S | N.A. | SI | HILO | 
| BTC_MVM_THP_TYP_VAL | S | Toma el Valor 1 | SI | TIPO DE MOVIMIENTO BATCH | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DEL DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | DOCUMENTO DEL TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD TERCERO | 
| PRC_STS_VAL | S | **Inicialmente** Toma el valor 1 Sin Procesar | SI | SITUACION DEL PROCESO | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA MODIFICACION | 
