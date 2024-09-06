![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# CREAR MOVIMIENTO DIFERIDO - Proceso Masivo de Terceros ([enlace con visión técnica][Tecnica]) {#titulo}

En el catálogo maestro de control de los procesos diferidos del Módulo de Terceros se tiene que  registrar la información específica del Movimiento Diferido.

IMPORTANTE: La tabla de Control no solamente contiene información del Movimiento Diferido. Además, incluye información de la persona física o jurídica para la que se va a realizar una de las dos operaciones disponibles en el sistema para el Módulo de Terceros: Operación de Alta o Creación y Operación de Modificación del Tercero.

Los atributos específicos correspondientes a la **Creación del Movimiento Diferido** en este catálogo maestro son ...

### **Compañía**

Esta propiedad le indica al sistema el código de la compañía sobre la que se está realizando la definición del movimiento diferido de Terceros.

### **Identificador Proceso**

Esta propiedad le indica al sistema el código del Proceso Diferido que identificará el Tercero o conjunto de Terceros que se van a tratar en la ejecución del Proceso.

### **Fecha Tratamiento del Proceso**

Este Atributo contiene la Fecha en la que se realiza la Ejecución del Proceso Diferido.

### **Número de Orden del Proceso** {#numero-de-orden-del-proceso}

Esta propiedad determina el orden en el que se se debe ejecutar la operación en el sistema.

### **Hilo del Proceso**

Este Atributo contiene el código del hilo en el que se va a ejecutar el registro puesto que en ocasiones, normalmente cuando el volumen de registros a tratar es masivo, la ejecución del proceso diferido necesita ser procesado de manera simultánea para acortar la ventana de tiempo de su ejecución.

---
[Tecnica]: <./02-Tecnica/CREAR-Movimiento-Diferido-TECNICA.md>