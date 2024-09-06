![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DETALLAR Información del Permiso de Conducir en el Movimiento Diferido del Tercero (**Visión Técnica**)

## **Modelo de datos involucrado**
La tabla que interviene en esta operación es:

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| T_THP_TRN_M_LCN                | TABLA BUZÓN LICENCIAS DE UN TERCERO                                                                 |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| IDN_VAL | S | N.A. | SI | IDENTIFICADOR | 
| IDN_SQN | S | N.A. | SI | SECUENCIA DENTRO DEL IDENTIFICADOR | 
| PRC_THD_VAL | S | N.A. | NO | HILO | 
| PRC_STS_VAL | S | N.A. | NO | SITUACIÓN DEL PROCESO | 
| CMP_VAL | S | N.A. | SI | COMPAÑÍA | 
| THP_DCM_TYP_VAL | S | N.A. | SI | TIPO DE COCUMENTO DEL TERCERO | 
| THP_DCM_VAL | S | N.A. | SI | CODIGO DE DOCUMENTO DEL TERCERO | 
| THP_ACV_VAL | S | N.A. | SI | ACTIVIDAD DEL TERCERO | 
| LCN_SQN_VAL | S | N.A. | SI | SECUENCIA DE LA LICENCIA | 
| LCN_TYP_VAL | S | N.A. | NO | TIPO DE LICENCIA | 
| LCN_VAL | S | N.A. | NO | CODIGO DE LICENCIA | 
| LCN_DAT | S | N.A. | NO | FECHA DE LICENCIA | 
| LCN_STS_VAL | S | N.A. | NO | ESTADO DE LA LICENCIA | 
| LCN_GRH_VAL | S | N.A. | NO | CODIGO GEOGRAFICO DE  EXPEDICION DE LA LICENCIA | 
| ACN_ORG_VAL | S | N.A. | NO | PRMERA ACCION QUE SE PRODUCE SOBRE EL REGISTRO ( (I)NSERTAR, (M)ODIFICAR  ) | 
| USR_VAL | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| MDF_DAT | S | N.A. | SI | FECHA DE ACTUALIZACION DE LA FILA | 
| ERR_IDN_VAL | S | N.A. | NO | CODIGO DE ERROR | 
| VAL_ZON_EXP_LIC_CON | S | N.A. | NO | ZONA GEOGRAFICA DONDE FUE EXPEDIDO EL CARNET DE CONDUCIR |