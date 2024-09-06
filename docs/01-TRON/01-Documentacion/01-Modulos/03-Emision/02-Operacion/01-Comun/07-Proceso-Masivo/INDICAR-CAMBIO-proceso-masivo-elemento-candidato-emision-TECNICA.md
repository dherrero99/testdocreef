![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

# INDICAR CAMBIOS elementos candidatos en Emisión (visión técnica)

## **Modelo de datos involucrado**
El modelo de datos que intervienen por operación se muestra a continuación

### G2000510

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| G2000510                       | PROCESOS MASIVOS                                                                                    |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| COD_CIA | N | N.A. | SI | COMPANIA | 
| FEC_TRATAMIENTO | N | N.A. | SI | FECHA EN LA QUE SE REALIZA EL PROCESO MASIVO | 
| NUM_ORDEN | N | N.A. | SI | NUMERO DEL PROCESO MASIVO | 
| TIP_MVTO_BATCH | N | N.A. | SI | TIPO DEL PROCESO MASIVO | 
| TXT_ALIAS | N | N.A. | NO | NOMBRE QUE SE QUIERA DAR AL PROCESO | 
| TIP_SITU_FILTRO | S | En esta operación toma varios valores dependiendo del momento. Los valores son 2-Filtrando y posteriormente 3-Ya filtrado | SI | SITUACION DEL MOVIMIENTO | 
| NOM_PRG_EXCEPCION | N | N.A. | NO | PROCEDIMIENTO DE EXCEPCION | 
| MCA_RECALCULA_FECHA | N | N.A. | SI | MARCA QUE INDICA SI SE TOMA COMO BASE LA FECHA QUE YA ESTA CALCULADO O SE VUELVE A CALCULAR | 
| TIP_FECHA_BASE | N | N.A. | NO | INDICA EN BASE A QUE FECHA SE HARA EL RECALCULO DE LA FECHA | 
| COD_USR | N | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| FEC_ACTU | N | N.A. | NO | FECHA DE ACTUALIZACION DE LA FILA | 
| TXT_MCA_PROCESO_ESTANDAR | N | N.A. | NO | APLICA PROCESO ESTANDAR | 
| IDN_PROCESO_PERSONALIZADO | N | N.A. | NO | IDENTIFICADOR DEL PROCESO MASIVO | 
