![Imagen LOGO](./00-Imagen/logo-TRON.png){ width="596" height="159" style="display: block; margin: 0 auto" }

# REVISAR Proceso Masivo TERCEROS

## Revisar el Resultado de la Ejecución del Proceso Diferido

Una vez ejecutado el proceso se tiene que comprobar el resultado en el Historial de Ejecución de la Tarea: Específicamente revisar el contenido del Campo **Nombre Tipo Situación**.

Si la ejecución ha terminado sin errores su valor será **“Terminación Normal”**, mientras que en caso contrario mostrará **"Terminación Anormal"**. En este caso se debe acceder al catálogo maestro de procesos diferidos de Terceros para conocer el valor del Atributo [Situación del Proceso](#situacion-del-proceso) además del detalle en el catálogo de control de errores de los procesos diferidos de Terceros.

Se deberán revisar los valores informados en las Tablas Buzón y corregir aquellos cuyas validaciones hayan provocado errores.

Tras ello se tendrá que [ejecutar nuevamente](./FORMACION-EJECUTAR-Proceso-Masivo-Terceros.md) el proceso diferido para llegar a su resultado final mediante la ejecución de aproximaciones sucesivas.

NOTA: La revisión del Proceso, hoy por hoy, se tiene que realizar con la participación del área de Tecnología de la empresa MAPFRE local.
