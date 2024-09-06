![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# FILTRAR póliza en emisión - Anulación por falta de pago

## **¿En que consiste?**
Determinar qué pólizas serán candidatas en un proceso masivo de Anulación por falta de pago.

## **Objetivo**
Extraer de la cartera aquellas pólizas que dispongan de al menos un **recibo que no haya sido cobrado** a la [fecha][FechaTratamiento] definida en el proceso masivo **más el [periodo de gracia][NoLink]** establecido y que **no se encuentre en el proceso de impagos**.

Para este proceso se toma el primer recibo no cobrado con una antigüedad mayor (por si existieran más recibos sin cobrar).

## **Proceso a seguir**
No es necesario realizar acción alguna ya que este es uno de los filtros que se encuentran establecidos por el núcleo de TRON.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[FechaTratamiento]: <../../CREAR-proceso-masivo-emision.md#fecha>
[PeriodoGracia]:    <>

[NoLink]: <../../../../../../../../NOLINK.md>