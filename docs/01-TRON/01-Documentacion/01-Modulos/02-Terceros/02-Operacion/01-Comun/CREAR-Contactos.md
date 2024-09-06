![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# CREAR Contactos del Tercero {#titulo}

## Objetivo

El propósito de esta pantalla es proporcionar la funcionalidad para que el Sistema pueda registrar todos los medios de contacto del Tercero.

# Contactos

![Datos Persona Física/Jurídica](./00-Imagen/Contactos.png)

    De Izquierda a Derecha y de Arriba hacia Abajo, los siguientes atributos marcan la secuencia de captura de la Información en el sistema.

### **Uso del Medio de Contacto**

Este atributo contiene una *clasificación* de los Usos posibles de los Medios de Contacto del Tercero, clasificación que ha de ser *definida/revisada* por parte de la entidad aseguradora para su posterior consideración y empleo en los procesos internos de la entidad.

A modo de ejemplo sus valores podrían ser:

| USOS.            |  Descripción |
| -----------      | -----------  |
| 001              | Personal     |
| 002              | Hogar        |
| 003              | Trabajo      |
| 004              | Principal    |
| 005              | Asistente    |
| 006              | Otro         |
| 007              | Familiar     |
| 008              | Bancaria     |
| 009              | Comercial    |

### **Secuencia del Medio de Contacto**

Este dato contiene el Número de Secuencia en la Captura de los Medios de Contacto del Tercero. Es un valor que se asigna automáticamente.

### **Tipo del Medio de Contacto**

Este atributo contiene el valor de la [clasificación](../../../../../../01-TRON/99-Terminos/TRON-Tipo-Terceros.md#cnh_typ_val) del Medio de Contacto del Tercero, clasificación que ha de ser *definida/revisada* por parte de la entidad aseguradora para su posterior consideración y empleo en los procesos internos de la entidad.

### **Clave/valor del Medio de Contacto**

Este Atributo contiene el valor real del Tipo del Medio de Contacto. Así pues, si se ha asociado en el contacto del Tercero el tipo 'Correo electrónico' el valor de este Dato tiene que tener el formato y contenido de un correo electrónico: xxxxxx@zzzzzz.zzz, en cambio, si se ha asociado al Tercero un tipo como 'Teléfono' el valor de este Dato tiene que tener el formato y contenido que correspondan a un Teléfono: < +99 99 9999 9999> (de acuerdo con las reglas de los Planes Nacionales de Numeración Telefónica de los Países.

### **Nombre del Medio de Contacto**

Este Atributo contiene el Nombre de la Persona que actúa como Medio de Contacto.

### **Primer y Segundo Apellido del Contacto**

Estos Campos contienen los Apellidos de la Persona que actúa como Medio de Contacto.

### **Tipo Documento**

Este Atributo del colapsador contiene el [tipo de documento] con el que se va a identificar a la persona física o jurídica como Contacto de acuerdo con los tipos de documentos que hayan sido configurados en el sistema previamente.

### **Clave del Documento**

Este Atributo del panel contiene la clave del documento que identifica a la Persona del Contacto.

### **Tipo de Cargo en la Empresa**

Este atributo contiene el valor de la [clasificación](../../../../../../01-TRON/99-Terminos/TRON-Tipo-Terceros.md#tip_cargo) de los cargos de las Personas en las Empresas, asociado al Contacto.

### **Cargo/Actividad del Contacto**

Este Campo contiene el código del Puesto con el que se estará identificando el Contacto del Tercero, de acuerdo con la relación de posibles valores existentes en el catálogo de [Cargos](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Cargo-en-Personas-Juridicas.md#titulo) existente en el Sistema.

### **Departamento del Contacto**

Este Campo contiene el código del departamento o sección con el que se estará identificando el Contacto del Tercero, de acuerdo con la relación de posibles valores existentes en el catálogo de [Departamentos en Personas Jurídicas](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Departamento.md#titulo) existente en el Sistema.

### **Clave del País**

Este Campo contiene el código del primer nivel de la estructura Geográfica (países) en el que se estará identificando el Medio de Contacto del Tercero, de acuerdo con la relación de posibles valores existentes en el catálogo de [Países](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/03-Estructura-geografica/DEFINICION-Nivel1-Estructura-Geografica.md/DEFINICION-Nivel1-Estructura-Geografica.md#titulo) existente en el Sistema.

### **Relación**

Esta cualidad se utiliza como texto libre para especificar la *relación* del Contacto con el Tercero.

### **Tercero de Referencia**

Este Dato indica que el Contacto es la Persona de Referencia (a la que se deben las notificaciones correspondientes) en el caso que se cumplan:

- El [Control en la Prevención del Lavado de Dinero](../../../../../../01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/DEFINICION-de-Compania.md#limite-de-primas) esté activado.
- El Tercero que se esté capturando sea una Persona Jurídica y además se haya indicado en la Información del Tercero que se le han de enviar notificaciones.

### **Medio de Contacto por Defecto**

Este Campo, en aquellos Terceros que tienen más de un medio de Contacto asociado, indicará cual de ellos es el que se debe considerar por defecto en los Procesos Operativos y/o Aplicaciones de la Entidad. Solamente puede haber uno identificado y marcado como tal por cada **Uso del Medio de Contacto** asignado.

### **Medio de Contacto Prioritario**

Este Campo, en aquellos Terceros que tienen más de un medio de Contacto asociado, va a indicar cual de ellos es el que se ha de considerar preferentemente en los Procesos Operativos de la Entidad. Solamente puede haber uno identificado y marcado como tal para el Tercero.

### **Medio de Contacto Validado**

Este Dato indica si el Medio de Contacto ha sido efectivamente validado, a efectos de calidad del dato, por la entidad aseguradora.

### **Inhabilitación**

Esta propiedad establece si el Medio de Contacto asociado al Tercero ha dejado de estar en vigor por lo que no debería ser considerado en ninguno de los procesos de la entidad.

### **Fecha de Validez**

Esta propiedad le indica al sistema la fecha a partir de la cual el Medio de Contacto va a ser plenamente operativo por lo que su correcto uso permite tener un histórico de los cambios efectuados en la Información del Medio de Contacto del Tercero

### **Observaciones**

Este Atributo permite capturar texto plano para ampliar o detallar la información del Medio de Contacto del Tercero.

### **Calidad**

Este Campo va a permitir capturar el [código de calidad](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Codigo-de-Calidad.md#titulo) que se va a asociar al Tercero de acuerdo a los valores codificados en el catálogo maestro existente en el Sistema, en el momento de registrarlo como Tercero No Deseado.

### **Estado**

Este atributo contiene una *clasificación* de los Estados de Identificación del Tercero como Tercero No Deseado, clasificación que ha de ser definida por parte de la entidad aseguradora para su posterior consideración y empleo en los procesos internos de la entidad.

A modo de ejemplo sus valores podrían ser:

| FORMATO.         |  Descripción    |
| -----------      | -----------     |
| 001              | Temporal        |
| 002              | Permanente      |
| 003              | Parcial         |
| 004              | Total           |
| ...              | ...             |

### **Causa**

Este Campo contiene el código del motivo por el cual se está Inhabilitando al Tercero, de acuerdo a los valores codificados en el [catálogo maestro](../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Causa-de-Inhabilitacion-por-Actividad.md#titulo) de causas de inhabilitación por código de actividad existente en el Sistema.

## Vínculos

## Preguntas frecuentes

## Audiencia

[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)

[tipo de documento]: <../../../../../../01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/01-Comun/DEFINICION-de-Documento-Identificativo.md>