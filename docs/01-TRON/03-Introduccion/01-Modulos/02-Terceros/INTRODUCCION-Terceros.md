![LOGO TRON](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# INTRODUCCIÓN - Módulo de TERCEROS {#titulo}

![Imagen Terceros](./00-Imagen/Definicion-de-Terceros.png "Documentación Terceros") 

## **Objetivo**

Dar de Alta a las personas físicas y jurídicas en el sistema configurado las diferentes **actividades** que éstas van a tener asociadas (para su empleo en los restantes módulos de la Solución en los que estas *personas* intervienen o pueden intervenir) parametrizando, clasificando y homogeneizando su información.

Los Terceros son sinónimos de Personas Físicas o Jurídicas.

- [Características del Módulo                  ](#caracteristicas-del-modulo)
- [Principales Conceptos                       ](#principales-conceptos)
- [Integración y Dependencias con Otros Módulos](#integracion-y-dependencias-con-otros-modulos)

## **Características del Módulo** {#caracteristicas-del-modulo}

### Clasificación

Todo Tercero como Persona física o Jurídica se tiene que asociar a **una o varias clasificaciones** denominadas Actividades: Clientes, Empleados de la Entidad Aseguradora, Abogados, Peritos o expertos de valoración de Daños, Tramitadores de Siniestros, Brokers de Seguros, etcétera.

### Visión única y *"limpia"* del Cliente.

El módulo de Terceros **habilita la visión única del Tercero** con los mejores datos del mismo a través de reglas de unificación, normalización y estandarización para ser empleados por todas las áreas de Negocio de la Organización mejorando así la interacción y gestión del Cliente.

### Mejor Experiencia del Cliente

El módulo de Terceros posibilita que durante las interacciones con el Cliente y los Servicios prestados al mismo, la entidad Aseguradora se dirija con **información sincronizada y coherente** generando percepción de calidad y una atención personalizada.

### Afinidad de los Datos

Todas los Terceros que pertenecen a una misma actividad son afines o análogos en el sentido que poseen **información/datos comunes** a todos ellos, e.g: Todos los Agentes están asociados por defecto a una Oficina de la estructura comercial configurada en la entidad aseguradora, todos los Terceros Personas Físicas tienen al menos un Nombre y un Apellido, étc.

### Mejora de la Productividad

Disponer de información consolidada en un único y mismo punto, **evita que se requieran múltiples consultas o extracciones de información** de diferentes sistemas para disponer de información combinada y fiable del Tercero.

### Soporte a la Acción Comercial

Disponer de información no fragmentada del Tercero dota al área comercial de la entidad Aseguradora de **mayor conocimiento** de la **información relevante** del Cliente, de su negocio y sus interacciones con la compañía.

### Funcionalidad Reforzada

Un Módulo que en su evolución presenta **funcionalidad reforzada** para la identificación y gestión de los Terceros como Proveedores. 

### Histórico de Modificaciones

El módulo de Terceros permite identificar y consultar el histórico de modificaciones de los datos de un cliente, pudiendo visualizar en cada uno de los movimientos realizados, **las modificaciones específicas** realizadas respecto de los datos existentes previamente.

## **Principales Conceptos** {#principales-conceptos}

- [Actividades                ](#actividades)
- [Catálogos de Configuración ](#catalogos-de-configuracion)
- [Estructuras de Información ](#estructuras-de-informacion)

### **Actividades** {#actividades}

Son **clasificaciones** que o bien identifican al Tercero como miembro de un Grupo afín de Terceros o bien determinan el conjunto de trabajos o acciones organizadas que son realizados por una persona, una profesión o una entidad.

A modo de ejemplo, si capturamos en el sistema la información de una persona física y la identificamos en el sistema con la actividad asociada a un Intermediario o Agente, este código de actividad le permitirá entrar de manera automática en el proceso de devengo de comisiones de la entidad MAPFRE, proceso por el que percibirá una retribución económica consistente, entre otros conceptos, de una parte proporcional de las primas conseguidas en su labor comercial directa o a través de su intervención o colaboración. 

En cambio si a la misma persona la hubiéramos identificado en el sistema como un Perito o como un Empleado, por lo que tendría asignados códigos diferentes de actividad al código de actividad de Intermediario del ejemplo anterior, esta persona podría respectivamente estar involucrada en tareas específicas de asignación y peritaje dentro del proceso de Gestión de Siniestros y Prestaciones o beneficiarse automáticamente de un descuento comercial en la contratación de sus pólizas en el proceso de Emisión.

### **Catálogos de Configuración** {#catalogos-de-configuracion}

Son catálogos que se configuran en el modelo de datos del módulo de Terceros y que cuentan con **códigos/claves** que sirven para estandarizar la información en el proceso de alta o modificación de los datos de los Terceros, como por ejemplo:

- En caso de dar de alta a un Cliente uno de los catálogos identifica el perfil financiero del mismo.
- En caso de inhabilitación de un Tercero uno de los catálogos identifica el motivo por el que se le está inhabilitando.
- En caso de ingresar la información de un Cliente, uno de los catálogos indicaría el estado del carnet de conducir.
- etcétera.

### **Estructuras de Información** {#estructuras-de-informacion}

La relación de estructuras de Información en las que se puede almacenar la información del Tercero, estructuras que son **comunes** a las actividades, es:

- [Datos Básicos del Tercero             ](#datos-basicos)
- [Datos Identificativos                 ](#datos-identificativos)
- [Obligaciones Fiscales                 ](#obligaciones-fiscales)
- [Datos Personas Políticamente Expuestas](#datos-peps)
- [Contactos del Tercero                 ](#contactos)
- [Direcciones del Tercero               ](#direcciones)
- [Documentos Alternativos               ](#documentos-alternativos)
- [Representantes Legales                ](#representantes-legales)
- [Accionistas                           ](#accionistas)
- [Datos Bancarios                       ](#datos-bancarios)

#### Datos Básicos del Tercero {#datos-basicos}

Contiene los datos que identifican al Tercero como la Actividad que se le va a asociar, el Tipo de documento que lo identifica, el código asociado, étc.

#### Datos Identificativos {#datos-identificativos}

Contiene los Datos que identifican al Tercero como una Persona Física o Jurídica, su categoría, su régimen fiscal, étc.

#### Obligaciones Fiscales {#obligaciones-fiscales}

Contiene determinada información del Tercero cuando éste tiene obligaciones fiscales en otros países.

#### Datos Personas Políticamente Expuestas {#datos-peps}

Esta estructura identifica al Tercero como Persona Políticamente Expuesta o con una Persona Políticamente Expuesta con la que tenga un vínculo o esté relacionada.

#### Contactos del Tercero {#contactos}

El propósito de esta estructura es identificar y registrar en el Sistema todos los medios de contacto del Tercero.

#### Direcciones del Tercero {#direcciones}

Contiene la relación de posibles direcciones del Tercero como por ejemplo la dirección de su residencia, de su Oficina, de correspondencia, ...

#### Documentos Alternativos {#documentos-alternativos}

Contiene la relación de posibles documentos alternativos con los que se puede identificar al Tercero.

#### Representantes Legales {#representantes-legales}

Esta estructura contiene la identificación e Información correspondiente a los Representantes Legales del Tercero.

#### Accionistas {#accionistas}

En el caso de que el Tercero sea una Persona Jurídica, esta estructura contendrá la relación de accionistas de la entidad y sus porcentajes accionariales.

#### Datos Bancarios {#datos-bancarios}

Contiene la información relativa a los medios de Cobro y Pago (Cuentas Bancarias, tarjetas,...) provistos por el Tercero.

---

Además y en el supuesto que que el Tercero se identifique en la Solución como un **Cliente/Asegurado** las estructuras de Información complementarias son:

- [Consentimientos del Tercero   ](#consentimientos)
- [Datos Asegurado No Deseado    ](#no-deseado)
- [Perfil Analítico del Tercero  ](#perfil-analitico)
- [Licencia/Permiso de Conducción](#licencia)

#### Consentimientos del Tercero {#consentimientos}

El propósito de esta estructura es la identificación de los Consentimientos del Tercero por los que acepta el tratamiento de los datos personales que le conciernen.

#### Datos Asegurado No Deseado {#no-deseado}

Contiene la información propia del Tercero, para uso interno por parte de la entidad aseguradora, por la que se considera al Tercero como un Tercero no Deseado.

#### Perfil Analítico del Tercero {#perfil-analitico}

El propósito de esta estructura de Información es recabar los datos del Perfil Analítico del Tercero de acuerdo con los cálculos efectuados localmente por la Entidad aseguradora.

Por ejemplo para identificar las probabilidades de up-selling, cross-selling o abandono del Tercero, étc.

#### Licencia/Permiso de Conducción {#licencia}

El propósito de esta estructura es la obtención de los datos específicos de la licencia o permiso de conducción del Tercero como por ejemplo su fecha de expedición/validez.

---

Por último y para **todas las Actividades de los Terceros** se han de informar los datos que son propios a la actividad asociada:

- [Información específica del Tercero](#datos-tercero)

#### Información Específica del Tercero {#datos-tercero}

Contiene la información propia del Tercero de acuerdo con la actividad que le representa. 

De esta manera y a modo de ejemplos:

- Si la actividad del Tercero corresponde a un Agente, se puede identificar la Oficina de la estructura comercial en la que este agente imputa las ventas de pólizas realizadas.

- Si la actividad del Tercero corresponde a un Cliente/Asegurado, se podría registrar si el Tercero cuenta o no con un Plan de Fidelización de la entidad Aseguradora.

- Si la actividad del Tercero corresponde a un Tramitador de Siniestros, se debe registrar el tipo de Tramitador que tiene asignado: Centro Telefónico, Recepcionista, Tramitador,...

- Si la actividad del Tercero corresponde a una Compañía Reaseguradora, se debe registrar qué tipo de entidad Reaseguradora es, su código de Rating, ...

## **Integración y Dependencias con otros Módulos** {#integracion-y-dependencias-con-otros-modulos}

Como *ejemplos* de integración y dependencia con los otros Módulos de la Solución ...

#### **Con el Módulo de COMUNES**

Determinados **Parámetros de la Instalación** modulan el comportamiento de la interfaz de la Solución para el Módulo de Terceros activando, desactivando o modificando los flujos de captura de su información (como ejemplo, no es igual la captura de un Cliente si este es persona física que si es una compañía) como tampoco es igual la captura de información de un Agente que la captura de los datos de un Asegurado.

#### **Con el Módulo de EMISIÓN**

En el proceso de Emisión se van a identificar tanto el Tomador/Contratante del Seguro como otros Terceros de acuerdo con la configuración del Producto. 

Por ejemplo, en Automóviles normalmente el Tomador del Seguro y el Asegurado coinciden en la misma persona pero dependiendo del país y la definición del producto puede ser necesario capturar la relación de posibles conductores, los beneficiarios del Seguro, étc.

#### **Con el Módulo de SINIESTROS**

En el proceso de Gestión de Siniestros se van a identificar por primera vez aquellas figuras que se determinen son necesarios para la gestión del Siniestro (como por ejemplo el conductor contrario o los posibles lesionados en el caso de una póliza de automóviles) o se van a utilizar los Terceros que fueron previamente identificados en la Emisión de la Póliza (Beneficiarios) para realizar el pago de las liquidaciones correspondientes.

#### **Con el Módulo de TESORERÍA**

En el Cobro de los Recibos se mostrará el Tomador de la Póliza o el Pagador del Recibo como la persona responsable del Pago de las Primas del Seguro (Tomador o Pagador que a su vez se capturó en el proceso de emisión de la póliza)

#### **Con el Módulo de CONTABILIDAD**

En el Asiento de Comisiones se muestran las liquidaciones realizadas al Agente responsable de la comercialización de la póliza, Agente que se identificó en la Emisión de la póliza.