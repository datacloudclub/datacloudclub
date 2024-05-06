# Cómo compartir mi proyecto con otras personas

## Objetivo

La presente guía muestra cómo compartir el presente proyecto con otras personas.

## Tabla de contenidos

* [Asignar un rol a otra cuenta](https://github.com/datacloudclub/datacloudclub/blob/main/Google%20Cloud%20Platform%20(GCP)/Gu%C3%ADas/uso_compartido_proyecto.md#asignar-un-rol-a-otra-cuenta)
* [Eliminar un rol asignado](https://github.com/datacloudclub/datacloudclub/blob/main/Google%20Cloud%20Platform%20(GCP)/Gu%C3%ADas/uso_compartido_proyecto.md#eliminar-un-rol-asignado)

## Asignar un rol a otra cuenta

En la consola de GCP: [http://console.cloud.google.com](http://console.cloud.google.com) nos dirigimos en el Menú de Navegación a IAM y administración:

![1714974595319](image/uso_compartido_proyecto/1714974595319.png)

Aquí podemos ver los roles asignados:

![1714974697365](image/uso_compartido_proyecto/1714974697365.png)

Para permitir a una persona pueda ver o realizar modificaciones al proyecto, le podemos asignar roles para darle acceso.

Hacemos click en "Otorgar acceso":

![1714974757366](image/uso_compartido_proyecto/1714974757366.png)

En Agregar principales, en "Principales nuevas *" escribimos el correo de Gmail de la persona que queremos autorizar.

![1714974843194](image/uso_compartido_proyecto/1714974843194.png)

Luego le asignamos un rol:

![1714974856010](image/uso_compartido_proyecto/1714974856010.png)

Para el presente caso, como es un conocido, le asignamos rol de "Propietario" para que tenga acceso completo a todos los recursos del proyecto, para que pueda crear nuevos recursos, eliminar otros, como si fuese el dueño de la cuenta.

Esta configuración pone en riesgo la integridad de la cuenta al dotar a otra persona con todas las habilidades del propietario, lo cual podría generar gastos sin nuestro control.

Se recomienda una lectura más detenida de los roles: [Referencias de IAM, roles básicos y roles predefinidos](https://cloud.google.com/iam/docs/understanding-roles).

![1714975031002](image/uso_compartido_proyecto/1714975031002.png)

Hacemos click en "Guardar" y luego podemos ver la modificación en la lista de roles asignados. Al ver un signo de alerta, se refiere a que se le envió un correo a la persona invitada para que acepte el rol designado, y de esta manera pueda adquirir el nivel de permiso elegido.

![1714975058098](image/uso_compartido_proyecto/1714975058098.png)

Un correo de estas características le llegará a la otra persona.

![1714975177598](image/uso_compartido_proyecto/1714975177598.png)

Al seguir el link enviado en el correo, nos llevará a GCP:

![1714975221547](image/uso_compartido_proyecto/1714975221547.png)

De esta manera, la otra persona va a poder ver al proyecto entre sus proyectos.

![1714975369279](image/uso_compartido_proyecto/1714975369279.png)

Haciendo click en la lista de proyectos podrá intercambiar entre proyectos.

![1714975348011](image/uso_compartido_proyecto/1714975348011.png)

## ¡Y listo! Así otra persona también puede introducir cambios a nuestro proyecto

Se recomienda leer con detención los roles que existen para poder determinar la cantidad justa de roles que le otorgamos a la otra persona.

Recuerda que los roles pueden ser cambiados en cualquier momento por el propietario del proyecto.


[volver a la Tabla de contenidos](https://github.com/datacloudclub/datacloudclub/blob/main/Google%20Cloud%20Platform%20(GCP)/Gu%C3%ADas/uso_compartido_proyecto.md#tabla-de-contenidos)


## Eliminar un rol asignado

Seleccionando la cuenta principal, hacemos click en Eliminar acceso:

![1714975536470](image/uso_compartido_proyecto/1714975536470.png)

Nos preguntará si queremos quitar a la cuenta asociada:

![1714975583607](image/uso_compartido_proyecto/1714975583607.png)

De esta manera se elimina el acceso de la cuenta:

![1714975645578](image/uso_compartido_proyecto/1714975645578.png)


[volver a la Tabla de contenidos](https://github.com/datacloudclub/datacloudclub/blob/main/Google%20Cloud%20Platform%20(GCP)/Gu%C3%ADas/uso_compartido_proyecto.md#tabla-de-contenidos)
