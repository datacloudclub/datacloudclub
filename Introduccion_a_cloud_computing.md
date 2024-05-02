# Introducción a Computación en la Nube

Tabla de contenidos

## Definición

En septiembre de 2011, el Instituto Nacional de Estándares y Tecnología (NIST: *National Institute of Standards and Technology*) dependiente de la Secretaría de Comercio de los Estados Unidos, definió "computación en la nube" (*cloud computing*) de la siguiente manera:

> La computación en la nube es un modelo para permitir el acceso a la red de manera ubicua (en todo tiempo y lugar), conveniente y bajo demanda a un conjunto compartido de recursos informáticos configurables (por ejemplo, redes, servidores, almacenamiento, aplicaciones y servicios) que se pueden aprovisionar y liberar rápidamente con un mínimo esfuerzo de gestión o interacción del proveedor de servicios.
>
> Este modelo de nube se compone de cinco características esenciales, tres modelos de servicio y cuatro modelos de implementación.

[Documento SP 800-145](https://csrc.nist.gov/pubs/sp/800/145/final)

### Características escenciales

* **Autoservicio on-demand:** Un consumidor puede apropiarse unilateralmente de capacidades informáticas, como procesamiento de un servidor o almacenamiento en red, según sea necesario de forma automática sin necesidad de intervención humana ni interacción con cada proveedor de servicios.
* **Amplio acceso a la red:** Las capacidades están disponibles en la red. Se acceden a ellas a través de mecanismos estandarizados que promueven el uso para plataformas heterogéneas de clientes ligeros o pesados (por ejemplo, teléfonos móviles, dispositivos portátiles, relojes, semáforos, heladeras o estaciones de trabajo).
* **Disponibilización de recursos compartidos:** Los recursos informáticos del proveedor se agrupan para servir a múltiples consumidores utilizando un modelo multi-inquilino. Los diferentes recursos físicos y virtuales son asignados y reasignados de forma dinámica según la demanda del consumidor. Hay una sensación de independencia de la ubicación, en el sentido de que el cliente generalmente no tiene control o conocimiento sobre la ubicación de los recursos proporcionados, pero es posible que pueda especificar la ubicación en un nivel superior de abstracción (por ejemplo, país, estado o centro de datos). Ejemplos de recursos incluyen almacenamiento, procesamiento, memoria y ancho de banda de red que se alojan en zonas o regiones.
* **Rápida elasticidad:** Las capacidades se pueden ser apropiadas y liberadas de forma elástica, en algunos casos automáticamente, para escalar rápidamente hacia afuera y hacia adentro de manera proporcional a la demanda. Desde el punto de vista del consumidor, las capacidades disponibles para ser utilizadas parecen ser infinitas e ilimitadas, pudiendo hacer uso de ellas en cualquier momento y cantidad.
* **Servicio medido:** Los sistemas en la nube controlan y optimizan automáticamente el uso de recursos aprovechando una capacidad de medición en algún nivel de abstracción apropiado para el tipo de servicio (por ejemplo, almacenamiento, procesamiento, ancho de banda y cuentas de usuario activas). El uso de recursos puede ser monitoreado, controlado y reportado, brindando transparencia tanto para el proveedor como para consumidor del servicio utilizado.


### Modelos de servicio

* **Software como servicio (SaaS):** La capacidad proporcionada al consumidor es la utlización de las aplicaciones del proveedor que se ejecutan en una infraestructura de nube. Se puede acceder a las aplicaciones desde varios dispositivos cliente a través de una interfaz de cliente ligero, como un navegador web (por ejemplo, correo electrónico basado en web), o una interfaz de programa. El consumidor no administra ni controla la infraestructura de la nube subyacente, incluida la red, los servidores, los sistemas operativos, el almacenamiento o incluso las capacidades de las aplicaciones individuales, con la posible excepción de ajustes limitados de configuración de aplicaciones específicas del usuario.
* **Plataforma como servicio (PaaS):** La capacidad proporcionada al consumidor es la implementación en la infraestructura de la nube de aplicaciones creadas o adquiridas por el consumidor creadas utilizando lenguajes de programación, bibliotecas, servicios y herramientas respaldados por el proveedor. El consumidor no administra ni controla la infraestructura de la nube subyacente, incluida la red, los servidores, los sistemas operativos o el almacenamiento, pero tiene control sobre las aplicaciones implementadas y posiblemente los ajustes de configuración para el entorno de alojamiento de aplicaciones.
* **Infraestructura como servicio (IaaS):** La capacidad proporcionada al consumidor es proporcionar procesamiento, almacenamiento, redes y otros recursos informáticos fundamentales donde el consumidor puede implementar y ejecutar software arbitrario, que puede incluir sistemas operativos y aplicaciones. El consumidor no gestiona ni controla la infraestructura de la nube subyacente, pero tiene control sobre los sistemas operativos, el almacenamiento y las aplicaciones implementadas; y posiblemente control limitado de componentes de red seleccionados (por ejemplo, firewalls de host).
* Véase también: Modelo de responsabilidad compartida
