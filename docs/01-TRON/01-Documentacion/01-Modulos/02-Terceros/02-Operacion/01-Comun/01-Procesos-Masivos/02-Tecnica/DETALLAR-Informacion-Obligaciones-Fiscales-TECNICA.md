![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DETALLAR Información Obligaciones Fiscales en el Movimiento Diferido del Tercero (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| ML_THP_NWT_XX_TXL_CNY          | TABLA BUZON PAISES CON OBLIGACIONES FISCALES                                                        |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| BTC_IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| SQN_VAL | S | N.A. | SI | SECUENCIA | 
| CMP_VAL | S | N.A. | SI | COMPANIA | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DEL DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | DOCUMENTO DEL TERCERO | 
| ADT_CNY_TXL_VAL | S | N.A. | SI | PAIS ADICIONAL CON OBLIGACION FISCAL | 
| IDN_TXP_ADT_CNY_TXL | S | N.A. | SI | IDENTIFICADOR CONTRIBUYENTE PAIS ADICIONAL | 
| RGS_DAT | S | N.A. | SI | FECHA DE ALTA | 
| DSB_ROW | S | N.A. | SI | FILA DESHABILITADA | 
| PRC_THD_VAL | S | N.A. | NO | HILO | 
| PRC_STS_VAL | S | N.A. | NO | SITUACION DEL PROCESO | 
| ACN_ORG_VAL | S | N.A. | NO | ACCION ORIGEN | 
| ERR_IDN_VAL | S | N.A. | NO | IDENTIFICADOR INTERNO DEL ERROR | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA MODIFICACION | 
