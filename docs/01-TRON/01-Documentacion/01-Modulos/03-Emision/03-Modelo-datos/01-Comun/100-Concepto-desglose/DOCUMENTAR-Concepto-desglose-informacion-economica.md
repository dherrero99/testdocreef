![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# Conceptos de desglose - Información económica {#titulo}

## **Objetivo**
Conocer cual es el contenido y el comportamiento de las columnas que contienen la información económica de una póliza/riesgo (marcadas en negrita).

## **Modelo de datos involucrado**

| TABLA | DESCRIPCIÓN |
|:--- |:--- |
| A2100170                       | CONCEPTOS DE DESGLOSE ECONÓMICO DE LA PÓLIZA                                                        |

######

| COLUMNA | COMENTARIOS |
| :---    | :---        |
| COD_CIA                        | COMPAÑÍA | 
| NUM_POLIZA                     | PÓLIZA | 
| NUM_SPTO                       | NUMERO DE SUPLEMENTO | 
| NUM_APLI                       | NUMERO DE APLICACIÓN | 
| NUM_SPTO_APLI                  | SUPLEMENTO DE LA APLICACIÓN | 
| NUM_RIESGO                     | RIESGO | 
| NUM_PERIODO                    | PERIODO (PARA PÓLIZAS MULTIANUALES) | 
| COD_COB                        | COBERTURA | 
| COD_DESGLOSE                   | CONCEPTO DE DESGLOSE ECONÓMICO | 
| COD_ECO                        | CONCEPTO ECONÓMICO DE RECIBO | 
| NUM_BLOQUE_ESTUDIO             | NO SE USA | 
| **IMP_ACUMULADO_ANUAL**        | **IMPORTE ACUMULADO ANUAL** | 
| **IMP_SPTO**                   | **IMPORTE DEL SUPLEMENTO** | 
| **IMP_NO_CONSUMIDO**           | **IMPORTE NO CONSUMIDO** | 
| **IMP_ANUAL**                  | **IMPORTE ANUAL** | 
| COD_RAMO                       | RAMO | 

A continuación y con el fin de entender mejor el sentido de las columnas que ocupan este documento, se establece unas bases para posteriormente realizar ejemplos:

Existe un concepto de desglose que, dependiendo de la edad del asegurado aplicará un recargo. Para ello se cuenta con la siguiente tabla que determina la edad y el monto a aplicar:

**Recargo por edad**

| EDAD  | RECARGO |
| :---: | :---:   |
| 15    | 150,00 |
| 16    | 160,00 |
| 17    | 170,00 |
| 18    | 180,00 |
| >18   | 200,00 |

## **Columnas**
### **IMP_ANUAL**
Importe que corresponde a un año de cobertura. Viene expresado con signo (positivo importe que MAPFRE recibirá, negativo importe que MAPFRE devolverá). Este importe ^^no interviene^^ en la generación de [cuotas][cuota].

Este importe ^^viene condicionado^^ por:

- La información del riesgo (en el ejemplo es la edad del asegurado)

Este importe ^^no viene condicionado^^ por:

- Los días de [vigencia][dias-vigencia] del [movimiento][tip-emision]
- Por el parámetro que determina en el ramo cuantos [días][mca_365_dias] tiene un año
- En caso de [movimiento][tip-emision] dentro del [periodo de vigencia][periodo-vigencia], el importe no consumido respecto a la situación anterior

#### **Ejemplo**
La información por la que viene condicionado el cálculo es:

| EDAD DEL ASEGURADO |
| :---: |
| 17    |

Con esta información, se muestran varios escenarios:

|ESCENARIO| EFECTO        | VENCIMIENTO     | IMP_ANUAL |
| :---:   | :---          | :---            |  ---:     |
| 1       | 01 enero 2023 | 01 enero 2024   | 170,00    |
| 2       | 01 enero 2023 | 01 octubre 2023 | 170,00    |
| 3       | 01 enero 2023 | 01 julio 2023   | 170,00    |
| 4       | 01 enero 2023 | 01 abril 2023   | 170,00    |

A continuación se muestra otro ejemplo:

| EDAD DEL ASEGURADO |
| :---: |
| 32    |

Con esta información, se muestran varios escenarios:

|ESCENARIO| EFECTO        | VENCIMIENTO     | IMP_ANUAL |
| :---:   | :---          | :---            |  ---:     |
| 1       | 01 enero 2023 | 01 enero 2024   | 200,00    |
| 2       | 01 enero 2023 | 01 octubre 2023 | 200,00    |
| 3       | 01 enero 2023 | 01 julio 2023   | 200,00    |
| 4       | 01 enero 2023 | 01 abril 2023   | 200,00    |

### **IMP_SPTO**
Monto a recibir o a devolver (el importe se expresa con signo) por parte de MAPFRE. Con este importe es con el que se crean posteriormente las [cuotas][cuota].

Este importe ^^viene condicionado^^ por:

- El importe anual (columna imp_anual), ya que es la base para determinar el valor de esta columna
- Los días de [vigencia][dias-vigencia] del [movimiento][tip-emision]
- Por el parámetro que determina en el ramo cuantos [días][mca_365_dias] tiene un año
- En caso de [movimiento][tip-emision] dentro del [periodo de vigencia][periodo-vigencia], el importe no consumido respecto a la situación anterior

Para hallar el importe del suplemento se utiliza el llamado [coeficiente de constitución][coef_cob] que determina cuanto del importe anual aplica en el [movimiento][tip-emision].

#### **Ejemplo**
La información por la que viene condicionado el cálculo es:

| IMPORTE ANUAL | DÍAS DE VIGENCIA | DÍAS AÑO | IMPORTE NO CONSUMIDO                             |
| ---:          | :---             | :---:    | :---                                             |
| 170,00        | Ver escenarios   | 365      | No aplica, este ejemplo es una emisión de póliza |

Con esta información, se muestran varios escenarios:

|ESCENARIO| EFECTO        | VENCIMIENTO     | DÍAS VIGENCIA | COEFICIENTE DE CONSTITUCIÓN | IMP_SPTO |
| :---:   | :---          | :---            | :---:         | ---:                        | ---:     |
| 1       | 01 enero 2023 | 01 enero 2024   | 365           | 1,000000                    | 170,00   |
| 2       | 01 enero 2023 | 01 octubre 2023 | 273           | 0,747945                    | 127,15   |
| 3       | 01 enero 2023 | 01 julio 2023   | 181           | 0,495890                    | 84,30    |
| 4       | 01 enero 2023 | 01 abril 2023   |  90           | 0,246575                    | 41,92    |

A continuación se muestra otro ejemplo donde cambia la definición de los [días año][mca_365_dias]:

| IMPORTE ANUAL | DÍAS DE VIGENCIA | DÍAS AÑO | IMPORTE NO CONSUMIDO                             |
| ---:          | :---             | :---:    | :---                                             |
| 170,00        | Ver escenarios   | 360      | No aplica, este ejemplo es una emisión de póliza |

Con esta información, se muestran varios escenarios:

|ESCENARIO| EFECTO        | VENCIMIENTO     | DÍAS VIGENCIA | COEFICIENTE DE CONSTITUCIÓN | IMP_SPTO |
| :---:   | :---          | :---            | :---:         | ---:                        | ---:     |
| 1       | 01 enero 2023 | 01 enero 2024   | 360           | 1,000000                    | 170,00   |
| 2       | 01 enero 2023 | 01 octubre 2023 | 270           | 0,750000                    | 127,50   |
| 3       | 01 enero 2023 | 01 julio 2023   | 180           | 0,500000                    | 85,00    |
| 4       | 01 enero 2023 | 01 abril 2023   |  90           | 0,250000                    | 42,52    |

### **IMP_ACUMULADO_ANUAL**
Contiene el importe que se obtendrá si se cobran todos los recibos generados en el [periodo de vigencia][periodo-vigencia]. Es decir, contiene la suma de la columna **IMP_SPTO** de todos los suplementos generados en el [periodo de vigencia][periodo-vigencia]. Esta columna se inicializa en la renovación de la póliza.

Para cada suplemento que se realiza, esta columna se halla de la forma:

| MOVIMIENTO    | FÓRMULA |
| :---          | :---    |
| Presupuesto      | IMP_ACUMULADO_ANUAL = IMP_SPTO |
| Declaración      | IMP_ACUMULADO_ANUAL = IMP_SPTO |
| Nueva póliza     | IMP_ACUMULADO_ANUAL = IMP_SPTO |
| Nueva aplicación | IMP_ACUMULADO_ANUAL = IMP_SPTO |
| Resto            | IMP_ACUMULADO_ANUAL = IMP_SPTO (suplemento actual) + IMP_ACUMULADO_ANUAL (suplemento anterior) |

#### **Ejemplo**
A continuación se muestra los importes de suplemento que se han generado en un [periodo de vigencia][periodo-vigencia]:

|SUPLEMENTO| IMP_SPTO |
| :---:    | ---:     |
| 20       | 170,00   |
| 21       | 127,50   |
| 22       | -85,00   |
| 23       |  42,52   |

Ahora se muestra el contenido de la columna IMP_ACUMULADO_ANUAL

|SUPLEMENTO| IMP_SPTO | IMP_ACUMULADO_ANUAL |
| :---:    | ---:     | ---:                |
| 20       | 170,00   | 170,00              |
| 21       | 127,50   | 297,50              |
| 22       | -85,00   | 212,50              |
| 23       |  42,52   | 250,02              |

### **IMP_NO_CONSUMIDO**
Conceptualmente es el importe que habría que devolver o cobrar (depende del signo), en caso que la información del riesgo haga que el concepto de desglose deje de aplicarse o varíe respecto a la situación anterior. Es decir, TRON simula una anulación cuando se realiza un suplemento previendo que las modificaciones que se realizarán hagan que varíe el importe o incluso hagan que el concepto de desglose no aplique.

Este importe se calcula siempre que se realiza un suplemento dentro del [periodo de vigencia][periodo-vigencia]. Hay suplementos que excepcionan la regla anterior. Estos son:

- Las [operaciones][operacion] que implican la renovación de una póliza ya que al ser un [periodo de vigencia][periodo-vigencia] nuevo, no hay que devolver o cobrar nada
- Los suplementos de tipo de [regularización][tip-spto-rg]

Este importe ^^viene condicionado^^ por:

- Para suplementos que NO anulan la póliza:

    - El importe anual (columna IMP_ANUAL) del movimiento anterior (no anulado [^no-anulado])

    - El llamado [coeficiente de constitución][coef_cob]

- Para suplementos que SI anulan la póliza:

    - El importe no consumido (columna IMP_NO_CONSUMIDO) del suplemento anterior (no anulado [^no-anulado])

    - El importe del suplemento (columna IMP_SPTO) del suplemento anterior (no anulado [^no-anulado])
    
    - El llamado [coeficiente de anulación][coef_anul]

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[^no-anulado]: Se refiere a un suplemento que no haya sido anulado, ya que un suplemento anulado, para TRON no existe

[periodo-vigencia]: <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#periodo-vigencia>
[dias-vigencia]:    <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#dias-vigencia>
[cuota]:            <../../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#cuota>
[operacion]:        <../../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#operacion>
[elemento]:         <../../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#elemento>
[tip-spto-rg]:      <../../../../../../../01-TRON/99-Terminos/TRON-tipo-emision.md#tip-spto>
[coef_cob]:         <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#coeficiente-constitucion>
[coef_anul]:        <../../../../../../../01-TRON/99-Terminos/TRON-Terminos-emision.md#coef-anulacion>
[mca_365_dias]:     <../../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#mca_365_dias>
[tip-emision]:      <../../../../../../../01-TRON/99-Terminos/TRON-tipo-emision.md#tip-emision>