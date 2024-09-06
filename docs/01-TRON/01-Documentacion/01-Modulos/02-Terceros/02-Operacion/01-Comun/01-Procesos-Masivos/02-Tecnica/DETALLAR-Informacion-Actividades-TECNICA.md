![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DETALLAR Información de Actividades en el Movimiento Diferido del Tercero (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| T_THP_TRN_M_ACV                | TABLA BUZÓN ACTIVIDADES DE UN TERCERO                                                               |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| IDN_SQN | S | N.A. | SI | SECUENCIA DENTRO DEL IDENTIFICADOR | 
| PRC_THD_VAL | S | N.A. | NO | HILO | 
| PRC_STS_VAL | S | N.A. | NO | SITUACIÓN DEL PROCESO | 
| CMP_VAL | S | N.A. | SI | COMPAÑÍA | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DE DOCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | CÓDIGO DE DOCUMENTO DEL TERCERO | 
| THP_VAL | S | N.A. | NO | CÓDIGO DE TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD DEL TERCERO | 
| PRN_DCM_TYP_VAL | S | N.A. | NO | TIPO DE DOCUMENTO PADRE DE UN TERCERO | 
| PRN_DCM_VAL | S | N.A. | NO | CÓDIGO DE DOCUMENTO PADRE DE UN TERCERO | 
| ACN_ORG_VAL | S | N.A. | NO | PRIMERA ACCION QUE SE PRODUCE SOBRE EL REGISTRO ( (I)NSERTAR, (M)ODIFICAR  ) | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA DE ACTUALIZACIÓN DE LA FILA | 
| ERR_IDN_VAL | S | N.A. | NO | CODIGO DE ERROR | 
| VLD_DAT | S | N.A. | NO | FECHA VALIDEZ | 
| RLT_THP_ACV_VAL | S | N.A. | NO | ACTIVIDAD DEL TERCERO RELACIONADO  | 
| RLT_THP_DCM_TYP_VAL | S | N.A. | NO | TIPO DEL DOCUMENTO DEL TERCERO RELACIONADO | 
| RLT_THP_DCM_VAL | S | N.A. | NO | DOCUMENTO DEL TERCERO RELACIONADO  | 
| RLN_TYP_VAL | S | N.A. | NO | TIPO DE RELACIÓN  | 
