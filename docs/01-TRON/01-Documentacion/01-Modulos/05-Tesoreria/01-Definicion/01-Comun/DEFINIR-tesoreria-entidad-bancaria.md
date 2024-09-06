![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

==EN CONSTRUCCIÓN==

[//]: # (## **FALTA: Revisar agrupación de propiedades, definición de varias propiedades, Ejemplos, imagenes, vínculos, preguntas frecuentes**)


# DEFINICIÓN de Entidad bancaria {#titulo}

## **Objetivo**
El objetivo es definir las características de las Entidades Bancarias con las que trabaja cada compañía para la gestión de recibos.

La Entidad Bancaria debe existir en la aplicación, como persona jurídica, asociada a la actividad que la identifica como Entidad Bancaria. 

Están relacionadas con el proceso de domiciliación bancaria, opción que los clientes pueden elegir para que se realice el cobro de sus recibos, descontando automáticamente de su tarjeta de crédigo o de su cuenta bancaria el importe de los mismos, a través de su Entidad Bancaria.

Para realizar este cobro automático, en la emisión de la póliza se debe identificar como tipo de gestor de cobro "DB" (Débito Automático en cuenta) o "TA" - (Débito con tarjeta de crédito).

- [Propiedades generales](#propiedades-generales)
- [Propiedades de tercero](#propiedades-de-tercero)
- [Propiedades de la entidad bancaria](#propiedades-de-la-entidad-bancaria)
- [Otras propiedades](#otras-propiedades)

## **Propiedades generales**
### **Compañía**
Este atributo contiene el código de la compañía para la que se está definiendo la entidad bancaria.

### **Entidad bancaria**
Este atributo será la clave con la que se identifica, en la aplicación, la entidad bancaria que se está definiendo.  

Ejemplo:  
- Entidad: 0037

### **Nombre entidad bancaria**
Este atributo contiene el nombre de la entidad bancaria que se está definiendo.

Ejemplo:  
- Entidad: 0037
- Nombre: BANCO NACIONAL

### **Nombre corto entidad bancaria**
Este atributo contiene el nombre de la entidad de forma abreviada.

Ejemplo:  
- Entidad: 0037
- Nombre: BANCO NACIONAL
- Nombre corto: B.NACIONAL

## **Propiedades de tercero**
### **Tipo de documento**
Este atributo contiene el tipo de documento de identidad con el que se identifica la Entidad Bancaria.

Ejemplo:  
- Tipo documento: CIF (Certificado de Identificación Fiscal)

### **Documento**
Este atributo contiene el código de documento de identidad con el que se identifica la Entidad Bancaria.

Este atributo, junto con el tipo de documento, serán la clave única para diferenciar la Entidad Bancaria como tercero no jurídico en la aplicación.

Ejemplo:  
- Tipo documento: CIF (Certificado de Identificación Fiscal)
- Documento: B123456789

### **Actividad**
Este atributo contiene la actividad con la que se identifica que el tercero de la aplicación es una Entidad Bancaria.

Ejemplo:  
- Tipo documento: CIF (Certificado de Identificación Fiscal)
- Documento: B123456789
- Actividad: 40 (entidad bancaria)

## **Propiedades de la entidad bancaria**
### **Tipo de entidad bancaria**
Este atributo clasifica la Entidad Bancaria, según el tipo de servicio que presta.

Ejemplo:  
- Tipo de entidad bancaria: 
    - BA (banco)
    - FE (financiera externa)
    - FP (financiera propia)

### **Código SWIFT**
Este atributo contiene el código que identifica a la entidad bancaria, utilizado en transferencias.

El código SWIFT (_Society for Worldwide Interbank Financial Telecommunication_) es un formato estándar para códigos de identificación de negocios. Se utiliza para identificar bancos e instituciones financieras globalmente, indicando quiénes son y dónde están. Es una especie de código bancario o de identificación.

Estos códigos se utilizan para transferir dinero entre bancos, en particular para transferencias internacionales

Ejemplo:  
- Código SWIFT: BBBBESMM000

### **Tipo domiciliacion**
Este atributo indica el tipo de servicio de domiciliación que la compañía tiene permitido realizar con la Entidad Bancaria, pudiendo ser: 

- C: Domiciliación con cuenta
- T: Domiciliación con tarjeta de crédito
- CT: Domiciliación con cuenta y tarjeta de crédito
- Sin valor: No se permite ningún tipo de domiciliación con la Entidad Bancaria

### **Tipo de institución bancaria**
<mark>Este atributo indica el tipo de instituación bancaria
tip_inst_bco	tipo de institucion bancaria	G1010031 (VALORES: 40-BANCO COMERCIAL 37-INSTITUCIÓN DE COBIERNO 90-PARICIPANTE DEL SPEI COMO BANCO )</mark>

<mark>cod_ref_bancaria	referencia bancaria	</mark>

<mark>fec_constitucion	fecha de constitucion de la empresa	<mark/>

<mark>cod_nacionalidad	nacionalidad	A100100 (cod_pais) ??? </mark>

<mark>cod_tipo_empresa_juridica	codigo de tipo de empresa juridica	</mark>

## **Otras propiedades**
### **Nombre localidad vernaculo**
Este atributo contiene el nombre del cuarto nivel de la estructura comercial, en leguaje local.

### **Inhabilitado**
Este atributo indica si la entidad bancaria está habilitada o no, para poder trabajar en la aplicación.


## **Vínculos**
[DEFINICION de compañía](/docs/01-TRON/01-Documentacion/01-Modulos/01-Comunes/01-Definicion/04-Estructura-producto/DEFINICION-Compania.md)

<mark>[DEFINICION de terceros](/docs/01-TRON/01-Documentacion/01-Modulos/02-Terceros/01-Definicion/)</mark>

[DEFINICION de gestor de cobro](/docs/01-TRON/01-Documentacion/01-Modulos/05-Tesoreria/01-Definicion/01-Comunes/DEFINICION-Gestor-cobro.md)

## **Preguntas frecuentes**
