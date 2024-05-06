# Descarga e instalación de Gcloud CLI para conectarme de manera remota a los servicios en la nube

## Objetivo

La presente guía muestra cómo utilizar las herramientas de desarrollador de Google Cloud SDK, en particular la interfaz de cliente Gcloud CLI.

Para más información, ver [la página de documentación oficial del Google Cloud SDK](https://cloud.google.com/sdk?hl=es-419).

## Tabla de contenidos

* [Descarga de Gcloud CLI]()
* [Instalación de Gcloud CLI]()

## Descarga de Gcloud CLI

Descargamos Gcloud CLI mediante el [siguiente link](https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe?hl=es-419).

## Instalación de Gcloud CLI

Para iniciar la instalación, ejecutamos el archivo descargado y veremos la siguiente pantalla:

![1715016315608](image/gcloud_cli_install/1715016315608.png)

La instalación es bastante sencilla, basta con darle siguiente a todas las ventanas hasta llegar a la última ventana previo a la instalación. Hacemos click en "Instalar" y comenzará la instalación.

![1715016343847](image/gcloud_cli_install/1715016343847.png)

Y la instalación fue realizada con éxito:

![1715016490926](image/gcloud_cli_install/1715016490926.png)

Hacemos click en "Siguiente" y por último en "Finalizar" para ejecutar el comando

```
gcloud init
```

para iniciar sesión en la cuenta de GCP.

![1715016499775](image/gcloud_cli_install/1715016499775.png)

Se abre una sesión en la terminal y debemos iniciar sesión en la cuenta de Gmail asociada a GCP:

![1715016759924](image/gcloud_cli_install/1715016759924.png)

Y deberemos aceptar los términos y condiciones:

![1715016807962](image/gcloud_cli_install/1715016807962.png)

![1715016830822](image/gcloud_cli_install/1715016830822.png)

Finalmente si el proceso fue exitoso, veremos este mensaje:

![1715016867607](image/gcloud_cli_install/1715016867607.png)

Mientras, en la sesión de la terminal abierta, ahora ya iniciada la sesión, nos pide el proyecto que queremos usar:

![1715016925745](image/gcloud_cli_install/1715016925745.png)

Allí seleccionamos el nombre del proyecto al que queremos ingresar, en este caso 1.

![1715016959030](image/gcloud_cli_install/1715016959030.png)

Después nos pregunta si queremos definir una Región y Zona por defecto, decimos que sí y elegimos la zona 8 (us-central1-a):

![1715017021290](image/gcloud_cli_install/1715017021290.png)

## ¡Y listo! Ya tenemos la línea de comando Gcloud CLI correctamente instalada y asociada al proyecto que queremos trabajar.
