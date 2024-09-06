![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# DEFINICIÓN de Tratamientos {#titulo}

## Propiedades Generales

En la definición del Ramo Técnico existen **tres propiedades** a las que denominaremos genéricamente ‘Tratamientos’, que identifican unívocamente la tipología o variante de los procesos de gestión de pólizas y contratos, gestión de siniestros y prestaciones y gestión Económica Financiera que se han de ejecutar al suscribir/emitir una póliza o un suplemento de este Ramo Técnico, gestionar un siniestro/expediente y contabilizar las primas de sus pólizas (Tratamiento de Emisión, Tratamiento de Siniestros y Tratamiento Contable respectivamente).

De esta manera estas tres propiedades permiten especializar la captura y gestión de la información de las pólizas en el sistema de acuerdo con sus valores asociados.

A modo de *ejemplo*,

- Si el Ramo técnico tuviera asociado un **tratamiento de emisión** de *Vida* estaríamos indicando al sistema que sus pólizas cubren seguros de personas y por tanto en el proceso de emisión se podría capturar información específica (como un cuestionario médico) o emitir suplementos específicos (como Suplementos de Aportaciones Extraordinarias o Rescates) que no podrán ser utilizados en cambio si el tratamiento de emisión correspondiera a un Ramo Técnico que cubriera seguros de daños materiales y por tanto tuviera asociado un tratamiento de *Diversos* o a un Ramo Técnico que cubriera seguros de Mercancías y por tanto tuviera asociado un tratamiento de *Transportes*. 

- De igual manera un ramo técnico cuyo **tratamiento de emisión** asociado fuera de *Automóviles* permitirá capturar en sus pólizas la relación e información de sus posibles ***accesorios*** a diferencia de los otros valores de esta propiedad (*Vida*, *Diversos* o *Transportes*) que no lo permitirían.

- En el caso del **tratamiento de siniestros**, el valor de la propiedad indica en el sistema la tipología o variante del proceso de gestión de siniestros y prestaciones que se ha de ejecutar sobre las pólizas pertenecientes al Ramo Técnico, siendo sus posibles valores los mismos que los indicados en la definición del tratamiento de emisión.

- De esta manera el sistema permite especializar la tramitación y gestión de los siniestros y sus expedientes en función de la tipología del tratamiento de siniestros asociado en el ramo técnico.

- Por último y en el caso del **tratamiento contable**, el valor indica la tipología o variante del proceso de gestión económica financiera que han de seguir los elementos económicos de las pólizas emitidas, siendo sus posibles valores los mismos que los de la propiedad tratamiento de emisión.

NOTA: El sistema permite que un Ramo Técnico tenga diferentes tipologías de tratamientos en los tres propiedades indicadas: tratamiento de emisión de *Diversos*, tenga en cambio un tratamiento de siniestros de *Automóviles* y un tratamiento contable de *Transportes*.

### **Tratamiento**

Esta propiedad define la clave con la que se identificará el Tratamiento en el Sistema.

`NOTA:` El catálogo de Tratamientos se entrega a las instalaciones **con su contenido ya prefijado.**

### **Descripción del Tratamiento**

Esta propiedad indica el nombre o la descripción del Tratamiento.

### **Abreviatura del Tratamiento**

Esta propiedad indica la abreviatura o descripción abreviada del Tratamiento.

Por tanto y como recopilación de las definiciones, el contenido del este catálogo es:

| TRATAMIENTO.   | NOMBRE            | ABREVIATURA  |
| :-----------:  | -----------       | -------      |
| A              | Automóviles       | Autos.       |
| D              | Diversos          | Div.         |
| T              | Transportes       | Trans.       |
| V              | Vida & Accidentes | Vida & Acc.  |

## Vínculos

Relación de Directrices y Documentos funcionales cuya lectura recomendada para evitar que la interpretación aislada del presente documento pueda conducir a error.

- [Configuración de Ramos/Productos](./DEFINICION-Ramo-Tecnico.md#titulo)

## Preguntas frecuentes

**(1)** ¿Existe alguna recomendación operativa que deba ser tomada en consideración localmente en la codificación, uso y definición de los Tratamientos en el Sistema?

**No es posible ampliar** en el sistema la relación de posibles valores de esta propiedad.

[Tabla TRON: G9990200]:<>