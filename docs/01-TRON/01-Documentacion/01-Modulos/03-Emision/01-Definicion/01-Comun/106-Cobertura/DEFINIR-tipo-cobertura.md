![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# DEFINICIÓN de tipo de cobertura {#titulo}

## **Objetivo**
Especifica el comportamiento de la cobertura en el proceso de emisión. Básicamente afecta a si aparece en el momento de la contratación, la suma asegurada y la prima, así como aquellos atributos que afectan a la definición relacionados con suma asegurada y prima.

Así por ejemplo, una cobertura puede que no disponga de suma asegurada. Esto implica que no será posible determinar ningún atributo que haga referencia a la suma asegurada, forma en la que revaloriza en la renovación, etc.

Los tipos que existen son:

| TIPO  | DESCRIPCIÓN |
| :---: | :---        |
| 1 | [INFORMATIVA](#Informativa) |
| 2 | [BÁSICA ADICIONAL](#Basica-adicional) |
| 3 | [REAL DEPENDIENTE](#Real-dependiente) |
| 4 | [REAL INDEPENDIENTE](#Real-independiente) |
| 5 | [SERVICIOS](#Servicios) |
| 6 | [CAPITAL ILIMITADO](#Capital-ilimitado) |
| 7 | [SINIESTROS](#Siniestros) |
| 8 | [FICTICIA RIESGO](#Ficticia-riesgo) |
| 9 | [FICTICIA PÓLIZA](#Ficticia-poliza) |
| R | [FICTICIA AJUSTE RIESGO](#Ficticia-ajuste-riesgo) |

## **Tipos**
### **Informativa** {#Informativa}
Este tipo realmente no se la considera cobertura, se utiliza como "separador" en la pantalla de contratación. Es simplemente un texto que aparecerá en la pantalla, por lo que cuando se defina en un ramo, no dispondrá de suma asegurada ni de prima.

Por ejemplo, si se tiene un ramo de hogar en el que existen coberturas que cubren el robo y el incendio** tanto para el continente como para el contenido, se puede utilizar este tipo de cobertura para crear una cobertura llamada **CONTINENTE** y otra cobertura llamada **CONTENIDO**. En una hipotética pantalla, y atendiendo al este ejemplo, quedaría de la siguiente forma (marcado en negrita e itálica):

| COBERTURA        | SUMA ASEGURADA | PRIMA    |
| :---             | ---:           | ---:     |
| ***CONTINENTE*** |                |          |
|  Robo            | 100.000,00     | 2.000,00 |
|  Incendio        |  80.000,00     |   600,00 |
| ***CONTENIDO***  |                |          |
|  Robo            | 200.000,00     | 1.000,00 |
|  Incendio        | 600.000,00     | 3.000,00 |

### **Básica adicional** {#Basica-adicional}
Es una cobertura que dispone de suma asegurada pero no dispone de prima. Está pensada para ofrecer su suma asegurada a otras coberturas. 

Variando el ejemplo del tipo de cobertura anterior ([Informativa](#informativa)), se puede realizar una definición de cobertura como **CONTINENTE** y otra como **CONTENIDO** que disponen de suma asegurada y, posteriormente las coberturas de Robo e Incendio tomarán la suma asegurada de la cobertura **CONTINENTE** y **CONTENIDO** respectivamente. El ejemplo (marcado en negrita e itálica) a continuación:

| COBERTURA        | SUMA ASEGURADA   | PRIMA    |
| :---             | ---:             | ---:     |
| ***CONTINENTE*** | ***100.000,00*** |          |
|  Robo            | 100.000,00       | 2.000,00 |
|  Incendio        |  80.000,00       |   600,00 |
| ***CONTENIDO***  | ***600.000,00*** |          |
|  Robo            | 200.000,00       | 1.000,00 |
|  Incendio        | 600.000,00       | 3.000,00 |

### **Real dependiente** {#Real-dependiente}
Una cobertura de este tipo, dispone de suma asegurada y de prima, pero la suma asegurada lo proporciona otra cobertura como debe ser [Básica adiciional](#Basica-adiciional) o [Real independiente](#Real-independiente). En la definición de producto, se verá que la suma asegurada que toma este tipo de cobertura puede ser un porcentaje de la cobertura de la cual dependa. Es decir, puede (por ejemplo), tomar un 80% de la suma asegurada de la cobertura de la que toma la suma asegurada.

Siguiendo con el ejemplo anterior, se va a suponer que la cobertura de **Incendio** toma la suma asegurada de la cobertura de **CONTINENTE** en un **80%**, y la otra cobertura de **Incendio** toma la suma asegurada de la cobertura de **CONTENIDO** en un **100%**. A continuación se muestra el resultado (en negrita e itálica):

| COBERTURA        | SUMA ASEGURADA   | PRIMA          |
| :---             | ---:             | ---:           |
| CONTINENTE       | 100.000,00       |                |
|  Robo            | 100.000,00       | 2.000,00       |
|  ***Incendio***  | ***80.000,00***  | ***600,00***   |
| CONTENIDO        | 600.000,00       |                |
|  Robo            | 200.000,00       | 1.000,00       |
|  ***Incendio***  | ***600.000,00*** | ***3.000,00*** |

### **Real independiente** {#Real-independiente}
Es una cobertura que dispone tanto de suma asegurada como de prima. La suma asegurada se define y en principio no depende de ninguna otra cobertura.

Siguiendo el ejemplo, se va a suponer que la cobertura de **Robo** (tanto de **CONTINENTE** como de **CONTENIDO**), disponen de su propio capital. A continuación se muestra el resultado (en negrita e itálica)

| COBERTURA        | SUMA ASEGURADA   | PRIMA          |
| :---             | ---:             | ---:           |
| CONTINENTE       | 100.000,00       |                |
|  ***Robo***      | ***100.000,00*** | ***2.000,00*** |
|  Incendio        |  80.000,00       |   600,00       |
| CONTENIDO        | 600.000,00       |                |
|  ***Robo***      | ***200.000,00*** | ***1.000,00*** |
|  Incendio        | 600.000,00       | 3.000,00       |

### **Servicios** {#Servicios}
Este tipo NO dispone de suma asegurada, pero dispone de prima. La contratación o no de este tipo de cobertura se conoce si aparece el valor "**INCLUIDA**" o "**EXCLUIDA**" en la pantalla de contratación. Para mostrar un ejemplo, se supone que existe una cobertura llamada Asistencia en viaje que estaría NO contratada y otra cobertura de Asistencia en el hogar que SI estaría contratada (en negrita e itálica)

| COBERTURA                    | SUMA ASEGURADA   | PRIMA        |
| :---                         | ---:             | ---:         |
| CONTINENTE                   | 100.000,00       |              |
|  Robo                        | 100.000,00       | 2.000,00     |
|  Incendio                    |  80.000,00       |   600,00     |
| CONTENIDO                    | 600.000,00       |              |
|  Robo                        | 200.000,00       | 1.000,00     |
|  Incendio                    | 600.000,00       | 3.000,00     |
| ***Asistencia en viaje***    | ***EXCLUIDA***   | ***0,00***   |
| ***Asistencia en el hogar*** | ***INCLUIDA***   | ***500,00*** |

### **Capital ilimitado** {#Capital-ilimitado}
Al tener una suma asegurada ilimitada, realmente no lleva asociado un valor específico por lo que en realidad es una cobertura tipo [servicio](#servicios). Es decir, sin suma asegurada, pero con prima. La diferencia radica en el literal que aparece en pantalla que muestra el valor "ILIMITADO". Por ejemplo, existe una cobertura llamada Asistencia médica que es de este tipo, la pantalla mostraría la información que se detalla a continuación (en negrita e itálica):

| COBERTURA               | SUMA ASEGURADA   | PRIMA    |
| :---                    | ---:             | ---:     |
| CONTINENTE              | 100.000,00       |          |
|  Robo                   | 100.000,00       | 2.000,00 |
|  Incendio               |  80.000,00       |   600,00 |
| CONTENIDO               | 600.000,00       |          |
|  Robo                   | 200.000,00       | 1.000,00 |
|  Incendio               | 600.000,00       | 3.000,00 |
| Asistencia en viaje     | EXCLUIDA         |     0,00 |
| Asistencia en el hogar  | INCLUIDA         |   500,00 |
| ***Asistencia médica*** | ***ILIMITADA***  |   700,00 |

### **Siniestros** {#Siniestros}
Este tipo, realmente no es una cobertura, por lo que no se muestra en la pantalla de contratación. Se utiliza con el fin de asociar tipos de expedientes que no necesitan de una cobertura en particular contratada para realizar  una prestación. Esto ocurre por ejemplo con los expedientes de convenio. Este tipo de expedientes se suelen asociar a este tipo de cobertura ya que toda la información de sininiestros queda asociado a esta cobertura pudiendo explotar información a este nivel (de cobertura).

### **Ficticia riesgo** {#Ficticia-riesgo}
Otro tipo que no es una cobertura y, que tampoco aparecerá en la pantalla de contratación. La utilidad de este tipo de cobertura es la de poder asociar información económica a nivel de riesgo. Hay que recordar que TRON permite disponer de pólizas con uno o varios riesgos. Hay ocasiones donde es necesario disponer de información económica agregada por riesgo (en vez de cobertura que es la asociación más natural). Cuando esto ocurre, los la información económica puede asociarse al riesgo mediante este tipo de cobertura. 
Un ejemplo podría ser cuando es necesario que los derechos de emisión se calculen por riesgo.

### **Ficticia póliza** {#Ficticia-poliza}
Este tipo de cobertura es parecido al tipo [ficticia riesgo](#Ficticia-riesgo), pero el ámbito de la información económica aplica a la póliza completa independientemente del número de riesgos que contenga la póliza. Un ejemplo podría ser que los impuestos se calculen a este nivel.

### **Ficticia ajuste riesgo** {#Ficticia-ajuste-riesgo}
Otro tipo de cobertura muy parecida a [ficticia riesgo](#Ficticia-riesgo) con la diferencia que esta cobertura va a ser la última que se calcule en el nivel riesgo.

## **Resumen**
Como compendio se muestra la siguiente tabla que refleja lo visto anteriormente

| TIPO | VISIBLE | CON SUMA ASEGURADA | CON PRIMA |
| :--- | :---:   | :---:              | :---:     |
| INFORMATIVA            | SI | NO | NO |
| BÁSICA ADICIONAL       | SI | SI | NO |
| REAL DEPENDIENTE       | SI | SI | SI |
| REAL INDEPENDIENTE     | SI | SI | SI |
| SERVICIOS              | SI | NO | SI |
| CAPITAL ILIMITADO      | SI | NO | SI |
| SINIESTROS             | NO | NO | NO |
| FICTICIA RIESGO        | NO | NO | NO |
| FICTICIA PÓLIZA        | NO | NO | NO |
| FICTICIA AJUSTE RIESGO | NO | NO | NO |


[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)
