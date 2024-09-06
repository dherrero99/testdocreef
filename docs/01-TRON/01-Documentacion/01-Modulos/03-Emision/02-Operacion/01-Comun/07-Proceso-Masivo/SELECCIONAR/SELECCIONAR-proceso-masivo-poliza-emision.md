![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

[//]: # (---)
[//]: # (tags:)
[//]: # (  - negocio)
[//]: # (  - analista)
[//]: # (  - implementador)
[//]: # (  - desarrollador)
[//]: # (---)

# SELECCIONAR póliza en emisión

## **¿En que consiste?**
Determinar qué pólizas serán candidatas a participar en el proceso masivo que se está definiendo.

## **Objetivo**
Extraer de la cartera solo aquellas pólizas con las que se pretende realizar la operación que se está definiendo

## **Proceso a seguir**
Existen tres formas en las que los [elementos][Elemento] pasen a ser candidatos y se incorporen al proceso masivo:

1. Movimientos prefijados en TRON
1. Herramienta de selección de pólizas/riesgos
1. Proceso personalizado de la instalación

### Movimientos prefijados en TRON
Existen movimientos que son capaces de determinar los [elementos][Elemento] que deben participar inicialmente en el proceso masivo. Estos movimientos son:

- [Renovación                   ][Renovacion] 
- [Anulación por falta de pago  ][Anulacion]
- [Regularización vida          ][RegularizacionVida]
- [Suspensión aportación pactada][SuspensionAportaciónPactada]
- [Recibos impagados            ][RecibosImpagados]

### Herramienta de selección de pólizas/riesgos
Existe una utilidad en TRON que permite establecer las reglas que seleccionen las pólizas y riesgos que participarían en el proceso masivo [FILTRAR póliza proceso masivo][FiltrarPolizaProcesoMasivo].

### Proceso personalizado de la instalación
Como última opción, la instalación puede crear sus propias lógicas que seleccionen las pólizas y riesgos a procesar.

[//]: # (## **Vínculos**)
[//]: # (## **Preguntas frecuentes**)

[Elemento]:      <../../../../../../../99-Terminos/TRON-Terminos.md#elemento>
[Operacion]:    <../../../../../../../99-Terminos/TRON-Terminos.md#operacion>

[FechaTratamiento]: <../CREAR-proceso-masivo-emision.md#fecha>

[Renovacion]:                   <./FILTRAR/FILTRAR-proceso-masivo-poliza-emision-renovacion.md>
[Anulacion]:                    <./FILTRAR/FILTRAR-proceso-masivo-poliza-emision-anulacion.md>
[RegularizacionVida]:           <./FILTRAR/FILTRAR-proceso-masivo-poliza-emision-regularizacion-vida.md>
[SuspensionAportaciónPactada]:  <./FILTRAR/FILTRAR-proceso-masivo-poliza-emision-suspension-aportacion-pactada.md>
[RecibosImpagados]:             <./FILTRAR/FILTRAR-proceso-masivo-poliza-emision-impago.md>

[FiltrarPolizaProcesoMasivo]:   <../SELECCIONAR/FILTRAR/FILTRAR-proceso-masivo-poliza-emision.md>
