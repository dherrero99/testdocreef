![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: Completar objetivo, Ejemplos, imagenes, vínculos a documentos, preguntas frecuentes**)

# DEFINICIÓN de Cajero {#titulo}

## **Objetivo**
El objetivo es identificar los usuarios de la aplicación que podrán tener acceso a las operaciones de tesorería y su contabilización.

- [Propiedades generales](#propiedades-generales)
- [Propiedades de acceso a entornos](#propiedades-de-acceso-a-entornos)
- [Propiedades del estado del cajero](#propiedades-de-estado-del-cajero)
- [Propiedades de auditoría](#propiedades-de-auditoría)

## **Propiedades Generales**
### **Compañía**
Este atributo contiene el código de la compañía para la que se está definiendo el cajero.

### **Cajero**
Este atributo contiene la clave con la que se identifica el cajero, será el mismo código con el que se identifica como usuario de la aplicación.

### **Nombre del cajero**
Este atributo contiene el nombre con el que se identifica el cajero, puede mantenerse el mismo nombre con el que se creó el usuario al darle de alta en la aplicación, o pude indicarse un nombre específico para identificar al cajero.

### **Tipo de cajero**
Este atributo contiene el código que identifica el tipo de cajero, pudiendo ser:

- P: Cajero principal  
- S: Cajero secundario

Por cada nivel 3 de la estructura comercial, debe existir un cajero principal y tantos secundarios como sea necesario.

El cajero principal es el único que puede cerrar el registro diario.

### **Tipo de reemplazo**
Este atributo indica si el cajero puede reemplazar al cajero principal, tomando los valores:

- P: Principal  
Este valor solamente se podrá indicar cuando el cajero es principal.  
- R: Reemplazante  
Se dará este valor a los cajeros secundarios que puedan reemplazar al cajero principal.
- Sin valor  
Indica que el cajero no puede reemplazar al cajero principal.

Si un cajero secundario, que puede ser reemplazante, entra en el parte contable antes que el cajero principal de la oficina comercial, éste tomará el rol de principal por ese día.

### **Último**
Este atributo indica si el cajero es el último principal de la compañía. 

Debido a que puede haber más de un cajero principal dentro de la compañía (uno por cada nivel 3 de la oficina comercial), es necesario indicar cuál de ellos es el último principal y por lo tanto, será el encargado de cerrar el registro diario, generando el asiento de tesorería del día.

Para poder cerrar el registro diario, todos los cajeros de la compañía deben haber cerrado y estar cuadrados.

Una vez cerrado el parte contable, el siguiente parte solo lo podrá abrir el cajero último principal con la nueva fecha de asiento.

### **Principal de nivel 2**
Este atributo indica si el cajero es principal para el nivel 2 de la estructura comercial, pudiendo consultar movimientos de los cajeros de todos los niveles 3 de su estructura comercial.

### **Fecha de valor**
Este atributo indica si el cajero puede modificar la fecha de los cobros, durante las operaciones de cobranza, para obtener el tipo de cambio, en los cobros en moneda extranjera.

### **Cajero central**
Este atributo indica si el cajero pertenece al nivel 3 de la estructura comercial que cada país tenga identificado como oficina central a nivel contable. Este cajero podrá pagar cualquier tipo de orden de pago (de siniestros, tesorería, agente, etc.).

### **Pago directo**
Este atributo indica si el cajero puede realizar el pago directamente desde la generación de la orden de pago.

### **Nivel 3 de la estructura comercial**
Este atributo contine el código del nivel 3 de la estructura comercial al que pertenece el cajero, es el que se le ha asociado cuando se le ha dado de alta como usuario de la aplicación.

### **Traspasos de caja a banco**
Este atributo indica si el cajero puede hacer traspasos de tesoreria de caja a banco.

### **Externo**
Este atributo indica si es un cajero externo, que es el que se utiliza para para procesos automáticos de cobro.

## **Propiedades de Acceso a entornos**
### **Entorno 1**
Este atributo indica si el cajero puede operar en el entorno 1 del registro diario (Cobros).

### **Entorno 2**
Este atributo indica si el cajero puede operar en el entorno 2 del registro diario (Generación de órdenes de pago).

### **Entorno 3**
Este atributo indica si el cajero puede operar en el entorno 3 del registro diario (Pago de órdenes de pago).

### **Entorno 4**
Este atributo indica si el cajero puede operar en el entorno 4 del registro diario (Anulación de órdenes de pago).

## **Propiedades de Estado del cajero**
### **Activo**
Este atributo indica si el cajero está dentro del registro diario (está activo) o no (no está activo).

### **Cuadrado**
Este atributo indica si el cajero está cuadrado, es decir, si todos los apuntes que ha realizados en el parte contable cuadran.

El valor de este atributo se actualiza en cada cierre, verificando que no exista diferencia entre el saldo acreedor y el saldo deudor de todas las operaciones realizadas por el cajero en el parte contable.

### **Entorno**
Este atributo contiene el código del último entorno del registro diario en el que ha trabajado el cajero.

Se actualiza en los procesos del registro diario.

### **Último número de recibo**
Este atributo contiene el último número de transacción que ha hecho el cajero en el entorno de cobros.

Se actualiza en los procesos del registro diario.

### **Última orden de pago**
Este atributo contiene el último número de transacción que ha hecho el cajero en el entorno de pago de órdenes de pago.

Se actualiza en los procesos del registro diario.

### **Último número de giro**
Este atributo contiene el último número de transacción que ha hecho el cajero en el entorno de generación de órdenes de pago.

Se actualiza en los procesos del registro diario.

### **Último número de anulación**
Este atributo contiene el último número de transacción que ha hecho el cajero en el entorno de anulación de órdenes de pago.

Se actualiza en los procesos del registro diario.

## **Propiedades de Auditoría**
### **Inhabilitado**
Este atributo indica si el cajero está habilitado o no, para poder trabajar. Un cajero inhabilitado no podrá acceder al registro diario de operaciones.

### **Fecha de alta**
Este atributo indica la fecha en la que el usuario de la aplicación se ha identificado como cajero.

### **Fecha de baja**
Este atributo contiene la fecha en la que se ha dado de baja (inhabilitado) el cajero.  

### **Observaciones**
Este atributo contine cualquier observación que se quiera incluir al inhabilitar el cajero, normalmente se utiliza para indicar el motivo por el cual se ha inhabilitado.

## **Vínculos**
[DEFINICION de compañía](/docs/01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-producto/DEFINICION-Compania.md)

<mark>[DEFINICION de estructura comercial]() </mark>

<mark>[Definición de usuarios aplicacación]()</mark>

## **Preguntas frecuentes**
