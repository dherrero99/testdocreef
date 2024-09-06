![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

# CREAR movimiento diferido en Emisión (visión técnica)

## **Modelo de datos involucrado**
Las tablas que intervienen en esta operación son:

### G2000510

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| G2000510                       | PROCESOS MASIVOS                                                                                    |

| COLUMNA | CAMBIA VALOR | MOTIVO/VALOR | OBLIGATORIA | COMENTARIO |
|:--- |:---: |:--- |:---: |:--- |
| COD_CIA | S | N.A. | SI | COMPANIA | 
| FEC_TRATAMIENTO | S | N.A. | SI | FECHA EN LA QUE SE REALIZA EL PROCESO MASIVO | 
| NUM_ORDEN | S | N.A. | SI | NUMERO DEL PROCESO MASIVO | 
| TIP_MVTO_BATCH | S | N.A. | SI | TIPO DEL PROCESO MASIVO | 
| TXT_ALIAS | S | N.A. | NO | NOMBRE QUE SE QUIERA DAR AL PROCESO | 
| TIP_SITU_FILTRO | S | Toma el valor 1-Sin filtrar | SI | SITUACION DEL MOVIMIENTO | 
| NOM_PRG_EXCEPCION | S | N.A. | NO | PROCEDIMIENTO DE EXCEPCION | 
| MCA_RECALCULA_FECHA | S | N.A. | SI | MARCA QUE INDICA SI SE TOMA COMO BASE LA FECHA QUE YA ESTA CALCULADO O SE VUELVE A CALCULAR | 
| TIP_FECHA_BASE | S | N.A. | NO | INDICA EN BASE A QUE FECHA SE HARA EL RECALCULO DE LA FECHA | 
| COD_USR | S | N.A. | SI | USUARIO QUE ACTUALIZO LA FILA | 
| FEC_ACTU | S | N.A. | NO | FECHA DE ACTUALIZACION DE LA FILA | 
| TXT_MCA_PROCESO_ESTANDAR | S | N.A. | NO | APLICA PROCESO ESTANDAR | 
| IDN_PROCESO_PERSONALIZADO | S | N.A. | NO | IDENTIFICADOR DEL PROCESO MASIVO | 
