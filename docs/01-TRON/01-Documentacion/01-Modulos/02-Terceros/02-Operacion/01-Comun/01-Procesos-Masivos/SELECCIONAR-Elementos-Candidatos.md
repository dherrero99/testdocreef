![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# SELECCIONAR ELEMENTOS CANDIDATOS - Proceso Masivo de Terceros ([enlace con visión técnica][Tecnica]) {#titulo}

En el catálogo maestro de control de los procesos diferidos del Módulo de Terceros también se tiene que registrar la información de identificación de la persona física o jurídica para la que se va a realizar una de las dos operaciones disponibles en el sistema del Módulo de Terceros: Operación de Alta o Creación y Operación de Modificación del Tercero.

Los atributos específicos correspondientes a la **Selección de los Elementos Candidatos** del Movimiento Diferido en este catálogo maestro son ...

### **Tipo del Movimiento en el Proceso**

Este Atributo especifica la [operación][Operacion] que se va a realizar en la ejecución del Tercero con respecto de la información contemplada en el Movimiento Diferido siendo sus posibles valores:

- Alta.
- Modificación.

NOTA: Las Modificaciones específicas para **Inhabilitar o Rehabilitar** un Tercero se deben implementar bajo el tipo de movimiento **Modificación**.

### **Tipo Documento Identificador del Tercero**

Esta propiedad identificará el tipo de Documento Identificador del Tercero.

### **Clave del Documento Identificador del Tercero**

Este atributo contendrá la clave del Tipo de documento Identificador asociado al Tercero.

### **Código de Actividad del Tercero**

Esta propiedad indica en el sistema el código de la Actividad del Tercero. 

### **Situación del Proceso** {#situacion-del-proceso}

Esta propiedad indica el estado de la Ejecución de la Operación definida para el Tercero candidato dentro del Movimiento Diferido, estado que inicialmente (antes de la ejecución del proceso) toma el valor '1'.

Sus posibles valores:

1. Sin Filtrar.
2. Detalle Filtrado.
3. Excepcionando.
4. Ya Excepcionado.
5. Ya Tratado.

---
[Tecnica]: <./02-Tecnica/SELECCIONAR-Elementos-Candidatos-TECNICA.md>
[Operacion]: <../../../../../../../01-TRON/99-Terminos/TRON-Terminos.md#operacion>