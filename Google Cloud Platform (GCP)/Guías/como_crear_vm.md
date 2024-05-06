# Creación de una instancia de máquina virtual

Podemos ingresar desde la Consola de GCP: [http://console.cloud.google.com](http://console.cloud.google.com).

![1714956162620](image/como_crear_vm/1714956162620.png)

En el botón de tres líneas horizontales de la parte superior izquierda vamos a encontrar el Menú de Navegación por los servicios:

![1714956199426](image/como_crear_vm/1714956199426.png)

Al final de la lista encontraremos la opción de ver todos los productos por si Compute Engine no aparece en la lista

![1714956207152](image/como_crear_vm/1714956207152.png)

Seleccionamos Compute Engine:

![1714956237970](image/como_crear_vm/1714956237970.png)

La primera vez que intentemos ingresar en nuestro proyecto, deremos habilitar la API del servicio de Compute Engine para poder hacer uso de todas sus funcionalidades y crear una máquina virtual.

![1714959156556](image/como_crear_vm/1714959156556.png)

Una vez que se encuentre habilitada la API, vamos a poder utilizar el servicio.

![1714959190909](image/como_crear_vm/1714959190909.png)

Dentro de Compute Engine, en Instancias de VM que es el servicio que se muestra de forma predeterminada, hacemos click sobre "Crear Instancia" para crear una nueva máquina virtual.

## Configurando la nueva máquina virtual

### Nombre, región y zona

La máquina virtual puede ser modificada posteriormente en cuanto a la cantidad de procesamiento y memoria que deseemos, la cantidad de memoria en el disco rígido asociado a ella, la configuración de la red e incluso su nombre.

Pero la elección de la región y la zona no puede ser modificada una vez creada la máquina virtual.

Elegimos:

* **Región**: us-central1 (Iowa)
* **Zona**: us-central1-a

![1714959236940](image/como_crear_vm/1714959236940.png)

El motivo de esta elección es que todos los servicios de GCP funcionan en una zona. No todos los servicios están disponibles en todas las zonas, como por ejemplo sucede con Sudamérica San Pablo o Santiago.

De manera que si queremos hacer uso de todos los servicios, deberemos elegir una zona donde estén todos disponibles. Además los procesos se llevan a cabo de manera remota. Por lo tanto, la interconexión entre los servicios en la nube se hará íntegramente en Iowa.

### Serie y tipo de máquina

La diferencia entre series depende de la cantidad de núcleos, la cantidad de memoria RAM y la potencia de las tarjetas gráficas asociadas a la máquina virtual.

En otras palabras, el precio que se paga por la máquina virtual, depende de la potencia que necesitemos.

De todas maneras, se puede modificar esta cantidad en cualquier momento posteriormente a su creación.

Elegimos la máquina E2 de tipo económico, es la Serie incluída en la capa gratuita.

Para aprovechar el crédito de prueba, podemos elegir cualquiera.

![1714959250218](image/como_crear_vm/1714959250218.png)

Nótese como al elegir distinto tipo de máquina, cómo varía el precio.

Tener en cuenta que el costo generado por la máquina virtual es mientras se encuentre encendida. Si la máquina virtual está apagada (se puede prender y apagar a voluntad) no genera gastos, pero el disco rígido asociado al ser persistente (que no se borra cuando se apaga la máquina sino que persiste) si genera gastos como figura en la siguiente imagen:

![1714959260360](image/como_crear_vm/1714959260360.png)

En cuanto al tipo de máquina, el tipo e2-micro está incluido en la capa gratuita. Pero para el presente ejemplo usaremos una e2-medium.

![1714959281459](image/como_crear_vm/1714959281459.png)

### Disco duro y sistema operativo

Para cambiar el sistema operativo y el tamaño del disco, hacemos click en el botón "Cambiar"

![1714959297879](image/como_crear_vm/1714959297879.png)

Elegimos la siguiente configuración:

![1714959307051](image/como_crear_vm/1714959307051.png)

* **Sistema operativo:** Ubuntu
* **Versión:** 24.04 LTS (la versión más reciente, también se puede probar la 20, 22, 23)
* **Tipo de disco de arranque:** disco persistente equilibrado
* **Tamaño (GB):** 30

Hacemos click en seleccionar para cerrar la ventana y confirmamos que los cambios fueron realizados.

![1714959346289](image/como_crear_vm/1714959346289.png)

[volver a la Tabla de contenidos](#tabla-de-contenidos)

### Configuraciones avanzadas de dirección IPv4 externa estática

Para el presente ejemplo no vamos a introducir más cambios con lo que podemos hacer click en "Crear".

Pero vale notar una configuración extra que puede ser de utilidad y comodidad. Puede ser modificada en cualquier momento.

Cada máquina virtual funciona con una dirección de IP interno de GCP, y una dirección de IP externa donde podemos conectarnos a ella vía remota.

La asignación de la dirección de IP es automática por ser "Efímera" es decir, que nos reserva una dirección IP global mientras la máquina esté encendida, pero al ser apagada, y luego reiniciada, la dirección de IP externa probablemente sea distinta.

Para reservar una dirección IP única para nosotros, GCP nos ofrece la creación de una IP personal (el costo es muy bajo, de US$ 0,10 por día).

![1714959358860](image/como_crear_vm/1714959358860.png)

Para asignarnos una dirección IP externa fija, desplegamos Opciones avanzadas, y luego en Herramientas de redes:

![1714959465502](image/como_crear_vm/1714959465502.png)

Buscamos donde dice Interfaces de red y desplegamos "default":

![1714959477329](image/como_crear_vm/1714959477329.png)

Casi en el fondo encontramos la dirección IPv4 externa, por definición es Efímera.

![1714959492147](image/como_crear_vm/1714959492147.png)

Haciendo click en dirección IPv4 externa podemos encontrar la opción para "Reservar dirección IP externa estática" para que sea fija.

![1714959510244](image/como_crear_vm/1714959510244.png)

Al hacer click en "Reservar Dirección IP Externa Estática, veremos el siguiente recuadro donde debemos asignar nombre a la dirección de IP reservada:

![1714959521019](image/como_crear_vm/1714959521019.png)

[volver a la Tabla de contenidos](#tabla-de-contenidos)

### Finalizar la configuración y crear la instancia

Antes de finalizar, podemos revisar el prespuesto estimado teniendo en cuenta si estuviese la instancia siempre encendida y a plena capacidad de consumo:

Siempre es aconsejable tener en cuenta la página oficial con respecto a los precios: [Página de precios de Compute Engine](https://cloud.google.com/compute/all-pricing)

![1714959652245](image/como_crear_vm/1714959652245.png)

Para finalizar podemos hacer click en "Crear" para crear la instancia

![1714959663624](image/como_crear_vm/1714959663624.png)

¡Felicitaciones! Hemos creado una instancia de máquina virtual.

![1714959679112](image/como_crear_vm/1714959679112.png)

Nótese la siguiente configuración de la instancia (este es mi ejemplo, en su caso serán otros valores).

* **Dirección IP interna**: 10.128.0.5
* **Dirección IP externa**: 34.135.38.214

Haciendo click en el botón **SSH**, se inicia en una ventana nueva la terminar para acceder a la instancia creada.

[volver a la Tabla de contenidos](#tabla-de-contenidos)
