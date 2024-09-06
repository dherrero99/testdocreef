![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DETALLAR Información de las Direcciones en el Movimiento Diferido del Tercero (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| ML_THP_NWT_XX_ADR              | TABLA BUZÓN DIRECCIONES DE TERCEROS                                                                 |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| BTC_IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| SQN_VAL | S | N.A. | SI | SECUENCIA | 
| CMP_VAL | S | N.A. | SI | COMPANIA | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DEL DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | DOCUMENTO DEL TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD TERCERO | 
| ADR_SQN_VAL | S | N.A. | SI | SECUENCIA DE LA DIRECCION | 
| VLD_DAT | S | N.A. | SI | FECHA VALIDEZ | 
| IDN_THP_VAL | S | N.A. | NO | IDENTIFICADOR TERCERO | 
| ADR_USE_TYP_VAL | S | N.A. | SI | TIPO USO DIRECCION | 
| DML_TYP_VAL | S | N.A. | SI | TIPO DOMICILIO | 
| ADR_TXT_VAL | S | N.A. | SI | DIRECCION | 
| ADR_NBR_VAL | S | N.A. | NO | NUMERO DE LA DIRECCION | 
| EXT_ADR_TXT_VAL | S | N.A. | NO | EXTENSION DIRECCION | 
| EXT_CNY_TXT_VAL | S | N.A. | NO | EXTENSION PAIS | 
| CNY_VAL | S | N.A. | NO | ZONA UNO GEOGRAFICA | 
| STT_VAL | S | N.A. | NO | ZONA DOS GEOGRAFICA | 
| PVC_VAL | S | N.A. | NO | ZONA TRES GEOGRAFICA | 
| TWN_VAL | S | N.A. | NO | ZONA CUATRO GEOGRAFICA | 
| PSL_COD_VAL | S | N.A. | NO | ZONA CINCO GEOGRAFICA | 
| LTT_VAL | S | N.A. | NO | LATITUD DE LA DIRECCION | 
| LNT_VAL | S | N.A. | NO | LONGITUD DE LA DIRECCION | 
| DFL_ADR | S | N.A. | SI | DIRECCION POR DEFECTO | 
| DSB_ROW | S | N.A. | SI | FILA DESHABILITADA | 
| ADR_CCK | S | N.A. | SI | DOMICILIO COMPROBADO | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA MODIFICACION | 
| PRC_THD_VAL | S | N.A. | NO | HILO | 
| PRC_STS_VAL | S | N.A. | NO | SITUACION DEL PROCESO | 
| ACN_ORG_VAL | S | N.A. | NO | ACCION ORIGEN | 
| ERR_IDN_VAL | S | N.A. | NO | IDENTIFICADOR INTERNO DEL ERROR | 
| OBS_VAL | S | N.A. | NO | OBSERVACIONES | 
| DIT_VAL | S | N.A. | NO | SUBCODIGO ZONA CUATRO GEOGRAFICA | 
| TAX_DML | S | N.A. | NO | DOMICILIO FISCAL | 