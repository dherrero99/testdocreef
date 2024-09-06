![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# DEFINICIÓN del formato del número de póliza {#titulo}

## **Objetivo**

El proceso de emisión de pólizas y contratos en TRON asocia de manera automática y unívocamente un código identificador a todas y cada una de las pólizas desde el momento que inicia el proceso de emisión. Si bien y
al término del mismo es factible modificar esta codificación de acuerdo a la definición del [ramo][ramo].

Existen algunos puntos a tener en cuenta:

- Existen unos elementos prefijados que pueden intervenir en el formato del número de póliza. Esta definición de formato se realiza por [sector][sector] y aplica a todos los ramos del sector definido
- El formato no se puede modificar una vez haya alguna póliza emitida de un sector
- El tamaño máximo del número de póliza es de 13 posiciones

Los elementos que pueden intervenir en el formato de póliza son:

| ELEMENTO | LONGITUD | ABREVIATURA |
| :---     | :---:    | :---:       |
| Compañía | 2        | C           |
| Sector   | 2        | S           |
| Ramo     | 3        | R           |
| Estructura comercial - primer nivel  | 2  | 1 |
| Estructura comercial - segundo nivel | 3  | 2 |
| Estructura comercial - tercer nivel  | 3  | 3 |
| Año                                  | 2  | A |
| Nº consecutivo                       | ¿? | N |

Existen unas reglas a cumplir cuando se define la formación del número de póliza:

1. El elemento número consecutivo (N) es obligatorio y la longitud de este elemento es el valor que falta para llegar a la longitud máxima del número de póliza (13) una vez descontados los elementos que forman el número
1. Al menos debe existir un elemento que forme parte de la numeración adicional al número consecutivo

Tomando los valores de las columnas abreviatura y longitud, se muestran ejemplos de formato:

- RRRAANNNNNNNN: Numeración formada por el ramo, año y consecutivo
- RRRAA222NNNNN: Numeración formada por el ramo, año, segundo nivel de la estructura comercial y consecutivo

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[ramo]:     <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-Ramo-Tecnico.md#titulo>
[sector]:   <../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-Producto/DEFINICION-de-Sector.md#titulo>