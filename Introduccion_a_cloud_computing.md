# Introducción a Computación en la Nube

## Tabla de contenidos

- [Definición](#definición)
  - [Características escenciales](#características-esenciales)
  - [Modelos de servicio](#modelos-de-servicio)
  - [Modelos de implementación](#modelos-de-implementación)
- [Servidores](#servidores)
- [Almacenamiento](#alamacenamiento)
- [Bases de Datos](#bases-de-datos)
- [Infraestructura Global](#infraestructura-global)
- [Regiones y Zonas de Disponibilidad](#regiones-y-zonas-de-disponibilidad)
- [Arquitectura en la nube](#arquitectura-en-la-nube)
- [Cloud Native](#cloud-native-maximizando-las-ventajas-del-cloud-computing)
- [Serverless](#serverless)
- [Lock-in en la Nube](#lock-in-en-la-nube)
- [Multi-Nube](#definición-y-estrategias-de-multi-nube)
- [Alta Disponibilidad y Tolerancia a fallos](#alta-disponibilidad-y-tolerancia-a-fallos)
- [Escalabilidad](#escalabilidad)

### Definición

En septiembre de 2011, el Instituto Nacional de Estándares y Tecnología (NIST: *National Institute of Standards and Technology*) dependiente de la Secretaría de Comercio de los Estados Unidos, definió "computación en la nube" (*cloud computing*) de la siguiente manera:

> La computación en la nube es un modelo para permitir el acceso a la red de manera ubicua (en todo tiempo y lugar), conveniente y bajo demanda a un conjunto compartido de recursos informáticos configurables (por ejemplo, redes, servidores, almacenamiento, aplicaciones y servicios) que se pueden aprovisionar y liberar rápidamente con un mínimo esfuerzo de gestión o interacción del proveedor de servicios.
>
> Este modelo de nube se compone de cinco características esenciales, tres modelos de servicio y cuatro modelos de implementación.

[Documento SP 800-145](https://csrc.nist.gov/pubs/sp/800/145/final)


### Características escenciales

* **Autoservicio on-demand:** Un consumidor puede aprovisionarse unilateralmente de capacidades informáticas, como procesamiento de un servidor o almacenamiento en red, según sea necesario de forma automática sin necesidad de intervención humana ni interacción con cada proveedor de servicios.
* **Amplio acceso a la red:** Las capacidades están disponibles en la red. Se acceden a ellas a través de mecanismos estandarizados que promueven el uso para plataformas heterogéneas de clientes ligeros o pesados (por ejemplo, teléfonos móviles, dispositivos portátiles, relojes, semáforos, heladeras o estaciones de trabajo).
* **Disponibilización de recursos compartidos:** Los recursos informáticos del proveedor se agrupan para servir a múltiples consumidores utilizando un modelo multi-inquilino. Los diferentes recursos físicos y virtuales son asignados y reasignados de forma dinámica según la demanda del consumidor. Hay una sensación de independencia de la ubicación, en el sentido de que el cliente generalmente no tiene control o conocimiento sobre la ubicación de los recursos proporcionados, pero es posible que pueda especificar la ubicación en un nivel superior de abstracción (por ejemplo, país, estado o centro de datos). Ejemplos de recursos incluyen almacenamiento, procesamiento, memoria y ancho de banda de red que se alojan en zonas o regiones.
* **Rápida elasticidad:** Las capacidades pueden ser aprovisionadas y liberadas de forma elástica, en algunos casos de forma automática, para escalar rápidamente hacia afuera y hacia adentro de manera proporcional a la demanda. Desde el punto de vista del consumidor, las capacidades disponibles parecen ser infinitas e ilimitadas, pudiendo hacer uso de ellas en cualquier momento y en cualquier cantidad.
* **Servicio medido:** Los sistemas en la nube controlan y optimizan automáticamente el uso de recursos aprovechando una capacidad de medición en algún nivel de abstracción apropiado para el tipo de servicio (por ejemplo, almacenamiento, procesamiento, ancho de banda y cuentas de usuario activas). El uso de recursos puede ser monitoreado, controlado y reportado, brindando transparencia tanto para el proveedor como para consumidor del servicio utilizado.


[volver a la tabla de contenidos](#Tabla-de-contenidos)


### Modelos de servicio

* **Software como servicio (SaaS):** La capacidad proporcionada al consumidor es la utlización de las aplicaciones del proveedor que se ejecutan en una infraestructura de nube. Se puede acceder a las aplicaciones desde varios dispositivos cliente a través de una interfaz de cliente ligero, como un navegador web (por ejemplo, correo electrónico basado en web), o una interfaz de programa. El consumidor no administra ni controla la infraestructura de la nube subyacente, incluida la red, los servidores, los sistemas operativos, el almacenamiento o incluso las capacidades de las aplicaciones individuales, con la posible excepción de ajustes limitados de configuración de aplicaciones específicas del usuario.
* **Plataforma como servicio (PaaS):** La capacidad proporcionada al consumidor es la implementación en la infraestructura de la nube de aplicaciones creadas o adquiridas por el consumidor creadas utilizando lenguajes de programación, bibliotecas, servicios y herramientas respaldados por el proveedor. El consumidor no administra ni controla la infraestructura de la nube subyacente, incluida la red, los servidores, los sistemas operativos o el almacenamiento, pero tiene control sobre las aplicaciones implementadas y posiblemente los ajustes de configuración para el entorno de alojamiento de aplicaciones.
* **Infraestructura como servicio (IaaS):** La capacidad proporcionada al consumidor es proporcionar procesamiento, almacenamiento, redes y otros recursos informáticos fundamentales donde el consumidor puede implementar y ejecutar software arbitrario, que puede incluir sistemas operativos y aplicaciones. El consumidor no gestiona ni controla la infraestructura de la nube subyacente, pero tiene control sobre los sistemas operativos, el almacenamiento y las aplicaciones implementadas; y posiblemente control limitado de componentes de red seleccionados (por ejemplo, firewalls de host).
* Véase también: [Modelo de responsabilidad compartida]()


[volver a la tabla de contenidos](#Tabla-de-contenidos)


### Modelos de implementación

* **Nube privada:** La infraestructura de la nube se proporciona para uso exclusivo de una única organización que comprende múltiples consumidores (por ejemplo, unidades de negocio). Puede ser propiedad de la organización, un tercero o una combinación de ellos (tanto en temas de administración como operación), y puede existir dentro o fuera de las instalaciones. Este es el caso de las nubes "on premise" cuando una organización quiere tener control total sobre sus datos y la arquitectura que los utiliza.
* **Nube comunitaria:** La infraestructura de la nube se proporciona para uso exclusivo de una comunidad específica de consumidores de organizaciones que tienen inquietudes compartidas (por ejemplo, misión, requisitos de seguridad, políticas y consideraciones de cumplimiento). Puede ser propiedad de, administrada y operada por una o más organizaciones de la comunidad, un tercero o alguna combinación de ellos, y puede existir dentro o fuera de las instalaciones. Este tipo de nube es la más usual en términos de administración pública, donde se crean bases de datos y registros de los ciudadanos que deben ser resguardados para mantener la privacidad de los mismos. Por un lado, se disponibiliza una plataforma mantenida por la administración pública como un sistema electrónico de impuestos, y la comunidad puede acceder a su propia información sin tener acceso a información indebida.
* **Nube pública:** La infraestructura de la nube está preparada para uso abierto por parte del público en general. Puede ser propiedad de, administrada y operada por una organización empresarial, académica o gubernamental, o alguna combinación de ellas. Existe en las instalaciones del proveedor de la nube. Este es el caso de AWS, GCP y Azure, entre otras.
* **Nube híbrida:** La infraestructura de nube es una composición de dos o más infraestructuras de nube distintas (privada, comunitaria o pública) que siguen siendo entidades únicas, pero están unidas por tecnología estandarizada o patentada que permite la portabilidad de datos y aplicaciones (por ejemplo, explosión de nube para equilibrio de carga entre nubes). 

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Servidores

Son computadoras potentes que forman parte de una red y proporcionan diversos servicios a los usuarios y dispositivos conectados. Operan con sistemas operativos como Windows, Linux o MacOS, y ejecutan aplicaciones específicas según su función, como Apache, Nginx o IIS para servidores web, o aplicaciones especializadas como PlatziWallet para servicios financieros. La ubicación de estos servidores puede ser on-premises, es decir, en las instalaciones físicas de la empresa propietaria, o en la nube, alojados en infraestructuras proporcionadas por proveedores de servicios en la nube como AWS o Google Cloud. Los servidores están diseñados para manejar una gran cantidad de usuarios y proporcionar servicios consistentes y confiables.

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Alamacenamiento

 En cuanto al almacenamiento, actúan como repositorios centralizados de información, asegurando que los datos estén disponibles cuando sean necesarios. El almacenamiento en servidores se puede clasificar en tres tipos principales: por objetos, por archivos y por bloques.

* **El almacenamiento por objetos:** divide los datos en unidades discretas llamadas objetos, que incluyen archivos, imágenes y otros tipos de archivos estáticos. Este método es ideal para datos que no requieren una estructura de sistema de archivos tradicional y es ampliamente utilizado en entornos de nube debido a su escalabilidad y facilidad de acceso.

* **El almacenamiento por archivos:** organiza los datos en una estructura jerárquica de carpetas y archivos, similar a los sistemas de archivos en computadoras personales. Este tipo de almacenamiento es útil cuando se necesita compartir archivos entre múltiples servidores o usuarios.

* **Almacenamiento por bloques:** segmenta los datos en bloques, cada uno con un identificador único, y es comúnmente utilizado para sistemas de almacenamiento de alto rendimiento como los discos duros de servidores virtuales en la nube. Esta modalidad permite una gestión eficiente y flexible de los datos, ya que los bloques pueden ser distribuidos y reorganizados según sea necesario.

### Bases de Datos

En la era digital actual, las bases de datos en la nube se han convertido en un componente esencial para la gestión eficiente de la información. Estas bases de datos ofrecen una variedad de modelos para satisfacer las necesidades específicas de almacenamiento y procesamiento de datos. A continuación, se presenta una descripción detallada de los tipos de bases de datos en la nube y sus aplicaciones.

* **Bases de Datos Relacionales:**
Las bases de datos relacionales son el pilar tradicional del almacenamiento de datos. Organizan la información en tablas interconectadas, donde cada tabla puede contener datos relacionados con otra, formando así una red compleja de información. Sistemas como MySQL, Oracle, PostgreSQL, MariaDB y SQL Server son ejemplos prominentes de bases de datos relacionales. Un caso de uso común es una tabla de usuarios vinculada a otra tabla que registra las tarjetas asociadas a cada usuario en un servicio.

* **Bases de Datos Clave/Valor:**
Este modelo no relacional almacena datos como pares clave-valor, donde cada clave es única y mapea a un valor específico. Estas bases de datos son altamente eficientes para operaciones de lectura y escritura rápidas y se utilizan comúnmente para gestionar sesiones de usuario y transacciones.

* **Bases de Datos en Memoria**
Las bases de datos en memoria utilizan la RAM del sistema para almacenar datos, lo que permite un acceso extremadamente rápido. Son ideales para aplicaciones que requieren una alta velocidad de procesamiento de datos, como sistemas de caché o análisis en tiempo real.

* **Bases de Datos Documentales**
MongoDB es un ejemplo prominente de bases de datos documentales. Estas bases de datos almacenan información en documentos, generalmente en formatos como JSON, lo que las hace perfectas para manejar grandes volúmenes de datos semi-estructurados y facilitar la integración con aplicaciones web.

* **Bases de Datos Columnares**
Optimizadas para el análisis de grandes conjuntos de datos, las bases de datos columnares organizan la información por columnas en lugar de filas. Esto mejora el rendimiento de las consultas y es especialmente útil en entornos de data warehousing, donde la integración y el análisis de datos son críticos.

* **Bases de Datos de Grafos**
Las bases de datos de grafos representan datos en forma de nodos y aristas, lo que permite modelar relaciones complejas y realizar análisis de redes. Son fundamentales para identificar patrones de conexión y analizar las interacciones dentro de redes sociales o sistemas recomendadores.

Cada tipo de base de datos en la nube tiene su conjunto único de ventajas y casos de uso. La elección entre ellas dependerá de los requisitos específicos de rendimiento, escalabilidad y tipo de datos a gestionar. Con la tecnología en constante evolución, es crucial mantenerse informado sobre las últimas tendencias y desarrollos en el campo de las bases de datos en la nube. Una opción es [revisar aquí](https://db-engines.com/en/ranking).

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Infraestructura Global

La infraestructura global de servicios en la nube es un componente crucial en la era digital actual, proporcionando una base sólida para la implementación de aplicaciones a escala mundial. Esta infraestructura se compone de una red de servidores altamente conectados, que utilizan la última tecnología e innovaciones en hardware para garantizar un rendimiento óptimo. Proveedores como AWS, Azure y Google Cloud Platform (GCP) han establecido una presencia global, con infraestructura distribuida en todo el planeta.

### Regiones y Zonas de Disponibilidad

Una región es una ubicación física específica donde se agrupan múltiples centros de datos. Estas regiones están estratégicamente distribuidas alrededor del mundo para ofrecer una cobertura global y reducir la latencia para los usuarios finales. Al seleccionar una región, es importante considerar factores como:

- **Latencia:** Buscar la región que ofrezca la mayor velocidad de respuesta para su audiencia objetivo.
- **Precio:** Los costos pueden variar significativamente entre diferentes países y regiones.
- **Catálogo de Servicios:** Aunque un proveedor de servicios en la nube puede ser el mismo, los servicios disponibles pueden variar entre regiones.

Las Zonas de Disponibilidad (AZ) son centros de datos individuales o grupos de estos que cuentan con su propia alimentación eléctrica, redes y conectividad redundante dentro de una región. Están interconectadas por redes de alta capacidad y baja latencia, lo que permite una comunicación eficiente. Una región puede tener varias AZ, cada una operando de manera independiente y aislada, asegurando que un fallo en una no afecte a las demás.

**Balanceadores de Carga y Alta Disponibilidad**

El balanceador de cargas juega un papel vital en la gestión de la infraestructura en la nube. Su función es distribuir el tráfico de solicitudes de manera equitativa entre las AZ dentro de una misma región. Esto es esencial para el diseño de aplicaciones multizona, permitiendo que la aplicación continúe funcionando sin interrupciones incluso si una AZ experimenta problemas. Gracias a esta característica, las aplicaciones pueden alcanzar un nivel de alta disponibilidad, manteniendo el servicio activo y accesible constantemente.

**Ejemplo Práctico**

Imaginemos una aplicación de comercio electrónico que atiende a clientes en América Latina. Para optimizar la latencia, se selecciona una región en Brasil, donde AWS tiene centros de datos. La aplicación se despliega en tres AZ distintas dentro de esta región. Un balanceador de cargas distribuye las solicitudes de los usuarios entre estas AZ. Si una de las AZ se ve afectada por un corte de energía, las otras dos pueden continuar manejando el tráfico, asegurando que la tienda en línea permanezca operativa.

**Conclusión**

La infraestructura global de servicios en la nube es una maravilla de la ingeniería moderna, permitiendo a las empresas desplegar aplicaciones resilientes y escalables. Con la correcta selección de regiones y el uso estratégico de zonas de disponibilidad y balanceadores de cargas, las organizaciones pueden garantizar una experiencia de usuario fluida y confiable, manteniendo sus aplicaciones disponibles en todo momento.

[volver a la tabla de contenidos](#Tabla-de-contenidos)

## Arquitecturas en la nube

* **La infraestructura como código (IaC):** es una práctica revolucionaria que transforma la manera en que las organizaciones despliegan y gestionan sus servicios en la nube. Al tratar la infraestructura de TI como si fuera software, se pueden aplicar técnicas de desarrollo de software, como el control de versiones, a la configuración y despliegue de servidores y otros recursos de red. Esto permite un despliegue más rápido, consistente y reproducible de entornos, lo cual es vital para aplicaciones que requieren una infraestructura ágil y confiable. **La implementación de IaC** significa que el servidor, junto con su almacenamiento y base de datos, se construirá y gestionará a través de código. Esto no solo facilita la automatización y la estandarización sino que también mejora la capacidad de reutilización gracias a los templates, que son plantillas de configuración predefinidas que pueden ser personalizadas y reutilizadas para diferentes proyectos o entornos.

* **Funciones serverless:** representan un paradigma de ejecución de código que libera a los desarrolladores de la gestión de servidores. Proveedores de nube como AWS con sus Lambda Functions, Azure con Azure Functions y Google Cloud con Cloud Functions ofrecen plataformas donde el código se ejecuta en respuesta a eventos específicos. Por ejemplo, en PlatziWalet, una función serverless podría activarse cuando un usuario sube una foto, ejecutando el código necesario para optimizar esa imagen automáticamente.

* **Contenedores Docker:** son otra pieza clave en la arquitectura moderna de aplicaciones. Un contenedor Docker es una unidad ejecutable que encapsula todo lo necesario para correr una aplicación, incluyendo el código, un runtime, herramientas del sistema, librerías y configuraciones, asegurando así que la aplicación se ejecute de manera uniforme en cualquier entorno. Esto es especialmente útil para PlatziWalet, ya que permite un despliegue consistente y escalable de la aplicación en diferentes entornos de nube.

* **Arquitectura de microservicios:** es un enfoque que estructura una aplicación como una colección de servicios pequeños e independientes, cada uno de los cuales realiza una función específica. En PlatziWalet, esto podría traducirse en microservicios dedicados a pagos, cobros, gestión de suscripciones, generación de códigos QR, y más. Cada microservicio es autónomo y puede ser desarrollado, desplegado y escalado independientemente, lo que resulta en una mayor flexibilidad y velocidad en el desarrollo y mantenimiento de la aplicación.

En resumen, la combinación de infraestructura como código, funciones serverless, contenedores Docker y microservicios ofrece una plataforma robusta y flexible para el desarrollo y despliegue de aplicaciones. Estas tecnologías permiten a los equipos de desarrollo centrarse en la creación de valor y la innovación, mientras que la infraestructura subyacente se gestiona de manera eficiente y escalable.

La adopción de la arquitectura Cloud Native representa una transformación significativa en el desarrollo y operación de aplicaciones, aprovechando las ventajas del cloud computing para mejorar la escalabilidad, elasticidad, seguridad y flexibilidad. A continuación, se presenta una versión mejorada y más detallada de la información proporcionada, con enlaces de interés incluidos.

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Cloud Native: Maximizando las Ventajas del Cloud Computing

El término "Cloud Native" se refiere a la construcción y ejecución de aplicaciones que explotan plenamente los beneficios del cloud computing. Estas aplicaciones están diseñadas desde cero para aprovechar servicios como la escalabilidad automática, la gestión de fallos, la distribución geográfica y la integración continua.

**Comparativa: Cloud Native vs. Aplicaciones Tradicionales**

- **Sistema Operativo**: En el enfoque Cloud Native, el sistema operativo se relega a un segundo plano, como en el caso de las arquitecturas serverless, donde la responsabilidad de la gestión del sistema operativo recae en el proveedor de servicios en la nube. Por el contrario, las aplicaciones tradicionales dependen en gran medida del sistema operativo, como Windows Server o Linux.

- **Desarrollo**: Las aplicaciones on-premises suelen seguir un modelo de desarrollo secuencial (Waterfall), mientras que Cloud Native adopta la entrega continua (Continuous Delivery), automatizando el despliegue, los servicios y la incorporación de nuevas características, lo que resulta en una mayor agilidad.

- **Escalabilidad**: La escalabilidad en entornos on-premises es manual y limitada por la capacidad del datacenter. En cambio, Cloud Native permite una escalabilidad automática utilizando tecnologías como serverless y contenedores.

- **Capacidad**: Las aplicaciones on-premises pueden resultar en sobreaprovisionamiento, por ejemplo, comprar diez servidores y utilizar solo dos. Cloud Native ofrece una capacidad de consumo y coste basada en el uso real.

- **Inmutabilidad y Predecibilidad**: Cloud Native proporciona inmutabilidad y elasticidad para manejar picos de demanda y errores, permitiendo desplegar servicios de forma rápida y completa. Esta ventaja no está presente en entornos on-premises.

**Cloud Native Computing Foundation (CNCF)**

La [CNCF](https://www.cncf.io/) es una fundación de software de código abierto que fomenta la adopción de la computación Cloud Native. Proyectos destacados incluyen ARGO para el despliegue de imágenes en clústeres de Kubernetes, ETCD y KUBERNETES para la orquestación de aplicaciones contenerizadas, FLUENTD y PROMETHEUS para la observabilidad y el monitoreo, y HELM para automatizar despliegues en KUBERNETES.

**Beneficios de una Aplicación Cloud Native**

Las aplicaciones Cloud Native ofrecen numerosos beneficios, como la capacidad de escalar recursos de manera rápida y dinámica, desarrollar y entregar código de calidad con mayor velocidad, y gestionar costos de manera eficiente, pagando solo por los recursos adicionales cuando son necesarios.

Para obtener más información sobre Cloud Native y cómo puede beneficiar a su organización, visite los siguientes enlaces de interés: Profundice mas con estos artículos.
[Whitestack](https://whitestack.com/es/blog/cloud-native/) | [AWS - Cloud Native](https://aws.amazon.com/es/what-is/cloud-native/)

La adopción de Cloud Native es un paso hacia un futuro más ágil, resiliente y eficiente en el uso de recursos para las aplicaciones empresariales.

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Serverless

La computación sin servidor, o serverless, es un paradigma de desarrollo y ejecución de aplicaciones que ha ganado popularidad en los últimos años debido a su eficiencia y escalabilidad. En este modelo, los proveedores de servicios en la nube, como AWS Lambda, Azure Functions y Google Cloud Functions, se encargan de la gestión de la infraestructura subyacente, permitiendo a los desarrolladores centrarse exclusivamente en el código y la lógica de negocio de sus aplicaciones.

**Definición de Serverless**
Serverless se refiere a la capacidad de ejecutar aplicaciones y servicios sin la necesidad de gestionar explícitamente servidores. En este modelo, el proveedor de la nube se encarga de las tareas de administración del sistema operativo, incluyendo el parcheo, la administración y la escalabilidad. Esto libera a los desarrolladores de la carga operativa y les permite desplegar su aplicación en contenedores serverless proporcionados por el proveedor, que son ejecutados en respuesta a eventos específicos o demandas de tráfico.

**Retos de Serverless**
A pesar de sus ventajas, la computación serverless presenta desafíos únicos:

- **Escalabilidad**: Aunque serverless ofrece una gran escalabilidad, está sujeta a las cuotas y límites establecidos por el proveedor de la nube. Por ejemplo, una función puede tener un límite de concurrencia, como 1000 ejecuciones concurrentes por segundo. Estos límites pueden ser ajustados mediante solicitudes de ampliación al proveedor de la nube.

- **Seguridad**: La seguridad en serverless se centra en proteger el código de la aplicación, especialmente en lo que respecta a la comunicación cifrada en tránsito. La seguridad del servidor en sí es manejada por el proveedor de la nube, lo que reduce la carga sobre el usuario.

- **Fiabilidad**: Los proveedores de la nube suelen comprometerse con altos niveles de disponibilidad, a menudo por encima del 99%, a través de Acuerdos de Nivel de Servicio (SLA) que garantizan una alta fiabilidad y disponibilidad del servicio.

- **Pago por uso**: El modelo de precios de serverless se basa en el tiempo de ejecución y la cantidad de recursos consumidos, como la memoria utilizada. Esto permite a los usuarios pagar únicamente por lo que utilizan, lo que puede resultar en ahorros significativos en comparación con la infraestructura tradicional.

- **Ahorro de tiempo y dinero**: La transición de entornos on-premises a serverless puede resultar en un ahorro considerable de tiempo y dinero, ya que elimina la necesidad de administrar o instalar servidores físicos.

- **Mejora de la productividad del desarrollador**: Los entornos serverless en la nube ofrecen servicios y herramientas que facilitan el testing local, la automatización del despliegue y las pruebas, mejorando la productividad del desarrollador.

Para obtener más información sobre la computación serverless y cómo puede beneficiar a su organización, puede consultar recursos como la documentación de AWS Lambda, Azure Functions, y Google Cloud Functions. Estos proveedores ofrecen guías detalladas y mejores prácticas para ayudar a los desarrolladores a aprovechar al máximo las capacidades serverless.

: https://aws.amazon.com/lambda/
: https://azure.microsoft.com/en-us/services/functions/
: https://cloud.google.com/functions/

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Lock-in en la Nube

* **"Vendor Lock-in:"** se refiere a la dependencia excesiva de un proveedor específico para obtener servicios o soluciones, lo que limita la capacidad de una organización para cambiar a otro proveedor sin incurrir en costos significativos o inconvenientes. Por ejemplo, una empresa que utiliza exclusivamente hardware y software de un proveedor puede enfrentar dificultades y gastos adicionales si decide migrar a tecnologías de otro fabricante.

* **"Product Lock-in:"** ocurre cuando una empresa o usuario está tan integrado con un producto o software específico que cambiar a otro producto se vuelve problemático. Un caso común es el uso de un formato de archivo propietario que no es compatible con otros programas, obligando al usuario a continuar utilizando el software original.

* **"Version Lock-in:"** se da cuando se depende de una versión específica de un producto y actualizar o cambiar a una nueva versión resulta difícil debido a incompatibilidades. Esto puede suceder, por ejemplo, cuando un sistema empresarial depende de una versión antigua de una base de datos y la actualización podría romper la funcionalidad de aplicaciones críticas.

* **"Architecture Lock-in:"** implica diseñar una arquitectura de tal manera que sea difícil realizar cambios debido a las profundas dependencias en componentes específicos. Un ejemplo sería una arquitectura de software que está tan estrechamente integrada con una infraestructura de nube específica que migrar a otra nube requeriría una revisión completa del sistema.

* **"Platform Lock-in:"** se produce cuando se está confinado a una plataforma específica, lo que dificulta la portabilidad de aplicaciones y servicios a otras plataformas. Esto puede verse en el desarrollo de aplicaciones móviles que están diseñadas exclusivamente para un sistema operativo, como iOS, lo que hace que la transición a Android sea un desafío.

* **"Skills Lock-in"** se refiere a tener personal con habilidades especializadas en una tecnología o plataforma específica, lo que complica la transición a diferentes tecnologías. Por ejemplo, un equipo de desarrolladores expertos en un lenguaje de programación obsoleto puede encontrar dificultades para adaptarse a nuevos lenguajes más modernos y demandados en el mercado.

* **"Legal Lock-in:"** se relaciona con estar limitado por acuerdos contractuales que restringen la capacidad de cambiar de proveedor o producto. Un ejemplo sería un contrato de licencia de software a largo plazo que impide a una empresa cambiar a soluciones de código abierto o de otro proveedor sin incurrir en penalizaciones.

* **"Mental Lock-in"** describe la tendencia a permanecer apegado a una tecnología o enfoque familiar, incluso cuando existen mejores alternativas disponibles. Esto puede manifestarse en la resistencia al cambio dentro de una organización, donde los empleados prefieren seguir utilizando herramientas o procesos con los que están cómodos en lugar de adoptar nuevas soluciones más eficientes.

Estos tipos de "lock-in" pueden tener un impacto significativo en la flexibilidad y la capacidad de innovación de una organización, y es crucial ser consciente de ellos al tomar decisiones estratégicas sobre tecnología y proveedores.

### Definición y Estrategias de Multi-Nube

La multi-nube es una arquitectura de TI que involucra el uso de servicios de más de un proveedor de nube pública para desplegar aplicaciones, plataformas o sistemas completos. Esta estrategia permite a las organizaciones seleccionar diferentes servicios de distintos proveedores para optimizar el rendimiento, los costos y la seguridad. Un ejemplo claro de esto es PlatziWallet, que opera en AWS mientras utiliza servicios en GCP, demostrando la flexibilidad y la capacidad de adaptación de las empresas multi-nube.

[volver a la tabla de contenidos](#Tabla-de-contenidos)

#### Estrategias de Multi-Nube

1. **Arbitrario**: Esta estrategia no se basa en decisiones técnicas sino en factores externos como acuerdos comerciales o MSA con el proveedor de nube, decisiones de negocios, o el conocimiento previo del equipo en una plataforma específica (skills lock-in), así como obligaciones contractuales (legal lock-in).

2. **Elección**: Implica seleccionar lo mejor de cada proveedor según el caso de uso específico. Esto requiere un análisis detallado de los pros y contras de cada proveedor de nube. Por ejemplo, una empresa puede optar por ejecutar su backend en AWS utilizando Kubernetes, mientras que las operaciones de DevOps se manejan en Azure. Esta elección puede llevar a un bloqueo con un proveedor (Vendor Lock-in) si se desea migrar servicios, ya que requeriría una reestructuración significativa.

3. **Agnóstico**: Busca la capacidad de desplegar servicios de aplicaciones de manera indistinta entre proveedores. Un caso de uso sería desplegar una aplicación en Kubernetes utilizando Open Source tanto en AWS como en Azure. La naturaleza de Kubernetes y Open Source facilita la replicación y reduce la dependencia de productos específicos (Lock-in).

4. **Paralelo**: Funciona como un plan de recuperación ante desastres (DRP), donde si un proveedor falla, otro toma el relevo. Esta estrategia es compleja y requiere personal altamente capacitado en múltiples nubes. Las empresas deben definir objetivos claros de tiempo de recuperación (RTO) y punto de recuperación (RPO).

5. **Segmentado**: Consiste en dividir las cargas de trabajo según la especialización del proveedor. Por ejemplo, ejecutar el backend en Azure y las operaciones de datos, análisis y aprendizaje automático en GCP. Esto puede generar un bloqueo de habilidades (skill lock-in) ya que el equipo necesita conocimientos específicos para cada segmento.

La adopción de una estrategia multi-nube ofrece a las empresas una mayor flexibilidad y aprovechamiento de las fortalezas de cada proveedor. Sin embargo, también conlleva desafíos como la gestión de la complejidad y el potencial lock-in. Es esencial que las organizaciones evalúen cuidadosamente sus necesidades y capacidades antes de implementar una estrategia multi-nube.

### Alta Disponibilidad y Tolerancia a fallos

La alta disponibilidad, la recuperación ante desastres y la tolerancia a fallos son conceptos cruciales en el mundo de la tecnología de la información. Estos principios son esenciales para garantizar que los sistemas y servicios críticos permanezcan operativos y accesibles, incluso frente a fallos y desastres imprevistos. A continuación, se presenta una explicación detallada de estos términos, junto con ejemplos y recomendaciones para su implementación.

**Alta Disponibilidad (High Availability - HA)**
La alta disponibilidad se refiere a la capacidad de un sistema para operar continuamente sin interrupciones significativas. Un sistema altamente disponible está diseñado para resistir fallos en sus componentes individuales y minimizar el tiempo de inactividad.

*Ejemplo:* Un sitio web de comercio electrónico que utiliza un clúster de servidores puede mantenerse en línea incluso si uno de los servidores falla, gracias a la redundancia incorporada en su arquitectura.

*Recomendación:* Para lograr una alta disponibilidad, es fundamental implementar redundancia en todos los niveles del sistema, desde el hardware hasta el software y la red.

**Tiempo de Recuperación Objetivo (Recovery Time Objective - RTO)**
El RTO es el tiempo máximo tolerable que un sistema puede estar fuera de servicio después de un fallo o desastre. Este parámetro ayuda a las organizaciones a planificar y prepararse para la recuperación de desastres.

*Ejemplo:* Una empresa financiera puede tener un RTO de 2 horas para su plataforma de transacciones en línea, lo que significa que el sistema debe restaurarse y estar operativo dentro de ese período después de una interrupción.

*Recomendación:* Para cumplir con el RTO establecido, es necesario tener un plan de recuperación de desastres bien definido y realizar pruebas periódicas para asegurar la eficacia del mismo.

**Punto de Recuperación Objetivo (Recovery Point Objective - RPO)**
El RPO define la cantidad máxima de datos que una empresa está dispuesta a perder en caso de una interrupción. Este valor se basa en la frecuencia de las copias de seguridad de los datos y su importancia para las operaciones del negocio.

*Ejemplo:* Un hospital puede tener un RPO de 5 minutos para su sistema de registros médicos electrónicos, lo que indica que las copias de seguridad deben realizarse al menos cada 5 minutos para evitar la pérdida de datos críticos.

*Recomendación:* Para alcanzar el RPO deseado, es crucial implementar soluciones de copia de seguridad y replicación de datos que se ajusten a las necesidades específicas de la organización.

**Tolerancia a Fallos (Fault Tolerance)**
La tolerancia a fallos es la habilidad de un sistema para seguir funcionando correctamente en el evento de un fallo en uno o más de sus componentes. Un sistema tolerante a fallos puede detectar y aislar el componente defectuoso y continuar operando sin interrupción.

*Ejemplo:* Un sistema de gestión de bases de datos distribuidas puede continuar procesando consultas y transacciones incluso si uno de los nodos de la base de datos falla, gracias a su diseño tolerante a fallos.

*Recomendación:* La implementación de la tolerancia a fallos requiere una planificación cuidadosa y una inversión en tecnologías que permitan la redundancia y la recuperación automática de fallos.

Estos conceptos son fundamentales para mantener la integridad y la disponibilidad de los sistemas informáticos en la actualidad. Al comprender y aplicar adecuadamente la alta disponibilidad, el RTO, el RPO y la tolerancia a fallos, las organizaciones pueden proteger sus operaciones críticas y ofrecer un servicio ininterrumpido a sus usuarios y clientes. Enlaces de Interés sobre disaster recovery. [AWS](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html) | [Azure](https://azure.microsoft.com/en-us/solutions/backup-and-disaster-recovery/) | [GCP](https://cloud.google.com/architecture/dr-scenarios-planning-guide?hl=es-419)

[volver a la tabla de contenidos](#Tabla-de-contenidos)

### Escalabilidad
La escalabilidad es un concepto crucial en el mundo de la tecnología, especialmente cuando se trata de aplicaciones y servicios web. Es la capacidad de un sistema para manejar un creciente número de demandas o para ampliar y reducir sus recursos para adaptarse a la carga de trabajo variable. Imagina que tienes una tienda en línea que ofrece descuentos significativos durante el Black Friday. La cantidad de usuarios que acceden a tu sitio aumentará exponencialmente, y necesitarás que tu infraestructura pueda manejar ese aumento sin interrupciones.

**Escalabilidad Vertical**
La escalabilidad vertical implica añadir más potencia a tu servidor existente, como más CPU, más memoria RAM o más espacio en disco. Es como si tuvieras un camión que transporta mercancías y, para llevar más carga, decides ponerle un motor más potente o una caja más grande. Sin embargo, hay un inconveniente: cada vez que actualizas el servidor, debes detenerlo temporalmente, lo que significa que tu servicio no estará disponible durante ese tiempo. Es como si tuvieras que detener el camión para cambiar el motor, y mientras tanto, no puedes entregar ninguna mercancía.

**Escalabilidad Horizontal**
Por otro lado, la escalabilidad horizontal se refiere a la adición de más servidores a tu sistema, en lugar de solo potenciar los existentes. Siguiendo con la analogía del camión, en lugar de un camión más grande, obtienes más camiones. De esta manera, si uno de los camiones necesita mantenimiento, los otros pueden continuar entregando las mercancías sin interrupción. Esta estrategia permite que tu servicio siga funcionando incluso mientras escalas, lo que se conoce como "no tener tiempo de inactividad".

**Escalabilidad y Alta Disponibilidad**
Ahora, podrías preguntarte si la escalabilidad es suficiente por sí sola. La respuesta es que la escalabilidad debe ir de la mano con la alta disponibilidad. Esto significa que tu servicio debe estar operativo y accesible en todo momento. Si escalas tu servicio pero solo en una zona geográfica y esa zona sufre un problema, como un corte de energía o un desastre natural, tu servicio completo podría caerse. Por lo tanto, es esencial distribuir tu servicio en múltiples zonas para garantizar que, incluso si una zona está inactiva, las otras puedan tomar el relevo y mantener tu servicio en funcionamiento.

**Ejemplos Adicionales**
Para ilustrar mejor estos conceptos, consideremos algunos ejemplos adicionales:

- **Escalabilidad Vertical**: Imagina que tienes una aplicación de edición de video que se usa intensamente durante la temporada de festivales de cine. Para prepararte para esta temporada alta, actualizas tus servidores con procesadores más rápidos y más memoria para manejar la carga adicional. Sin embargo, después del festival, reduces los recursos para ahorrar costes.

- **Escalabilidad Horizontal**: Piensa en una red social que experimenta un aumento de tráfico cada vez que lanza una nueva característica viral. Para manejar esto, automáticamente añaden más servidores a su clúster, permitiendo que más usuarios disfruten de la nueva característica sin ralentizar el servicio.

La escalabilidad no es solo una cuestión técnica, sino también una estrategia de negocio que asegura que tus usuarios tengan una experiencia fluida y sin interrupciones, independientemente de las fluctuaciones en la demanda. Al combinar la escalabilidad con la alta disponibilidad, puedes proporcionar un servicio confiable que se adapte a las necesidades cambiantes de tus usuarios y del mercado. Puedes profundizar un poco [AQUÍ](https://azure.microsoft.com/es-es/resources/cloud-computing-dictionary/scaling-out-vs-scaling-up/#overview).

[volver a la tabla de contenidos](#Tabla-de-contenidos)

# ¡Seguiremos actualizando contenido, visita esta página cada cierto tiempo!