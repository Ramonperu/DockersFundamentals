# Dockers fundamentals

Bienvenidos a la guía básica, para principiantes, sobre dockers realizada por Ramon Peinado Ruiz gracias al .

## CONCEPTOS BASICOs

### ¿Que es docker ?

Docker es una tecnología de contenedores que simplifica el proceso de desarrollo, implementación y administración de aplicaciones. Un contenedor es una unidad ligera y portátil que incluye todo lo necesario para ejecutar una pieza de software, incluyendo el código, las bibliotecas y las dependencias. Esto permite que las aplicaciones se ejecuten de manera consistente en cualquier entorno que admita Docker.

<img align="center" src="/img/1ºimagenn.PNG"  />

**Ventajas de Docker:**

- **Portabilidad y Consistencia:**
  - Los contenedores encapsulan todo lo necesario para ejecutar una aplicación, asegurando que se comporte de la misma manera en cualquier entorno.
  - Elimina el problema de "funciona en mi máquina" al garantizar que la aplicación se ejecute de la misma manera en el entorno de desarrollo, pruebas y producción.
- **Eficiencia de Recursos:**
  - Los contenedores comparten el núcleo del sistema operativo del host, lo que los hace ligeros en comparación con las máquinas virtuales tradicionales.
  - Permite ejecutar múltiples contenedores en un solo host, optimizando el uso de recursos y mejorando la eficiencia.
- **Despliegue Rápido:**
  - Los contenedores se inician en cuestión de segundos, lo que facilita la implementación rápida y escalable de aplicaciones.
  - Ideal para entornos de microservicios donde se despliegan múltiples servicios de forma independiente.
- **Aislamiento y Seguridad:**
  - Cada contenedor opera de manera aislada, compartiendo solo los recursos necesarios con el host.
  - Proporciona una capa adicional de seguridad al limitar el acceso a recursos y procesos del sistema.
- **Gestión Sencilla:**
  - Docker ofrece herramientas de gestión robustas que facilitan la construcción, el envío y la ejecución de contenedores.
  - Permite la orquestación de contenedores a través de herramientas como Docker Compose y Kubernetes.
- **Escalabilidad Horizontal:**
  - Los contenedores facilitan la escalabilidad horizontal, permitiendo agregar o quitar instancias de contenedores según la carga de trabajo.
  - Ideal para entornos dinámicos que requieren adaptabilidad a la demanda.
- **Entorno Reproducible:**
  - Dockerfiles permiten describir de manera precisa y reproducible todos los pasos necesarios para configurar un entorno.
  - Garantiza que todos los desarrolladores trabajen en el mismo entorno, evitando problemas de dependencias.
- **Comunidad Activa:**
  - Docker cuenta con una comunidad activa que contribuye con mejoras constantes y comparte conocimientos a través de foros y recursos en línea.

### Sistemas operativos:

Docker es compatible con una amplia variedad de sistemas operativos:

- **Linux:**
  - Docker tiene un soporte nativo en sistemas operativos Linux. Es especialmente eficiente en entornos basados en el kernel de Linux.
- **Windows:**
  - Docker Desktop está disponible para sistemas operativos Windows. Utiliza la virtualización a través de Hyper-V para crear un entorno de contenedores.
- **macOS:**
  - Docker Desktop también es compatible con macOS. Al igual que en Windows, utiliza la virtualización (en este caso, xhyve) para ejecutar contenedores en un entorno de macOS.
- **Cloud Platforms:**
  - Docker se utiliza extensamente en entornos de nube, como Amazon Web Services (AWS), Microsoft Azure y Google Cloud Platform (GCP). Puedes ejecutar contenedores Docker en máquinas virtuales en la nube.

### WSL o Windows Subsystem for linux:

Es una característica de Windows que permite ejecutar un entorno Linux directamente en un sistema operativo Windows. Básicamente, WSL proporciona una capa de compatibilidad que permite a los usuarios de Windows ejecutar binarios de Linux de forma nativa.

Ventajas y caracteristicas:

- **Entorno Linux en Windows:**
  - WSL permite ejecutar distribuciones de Linux, como Ubuntu, Debian y otras, directamente en un sistema Windows sin la necesidad de una máquina virtual.
- **Interoperabilidad:**
  - Facilita la interoperabilidad entre aplicaciones y herramientas diseñadas para Linux y el entorno Windows. Puedes ejecutar comandos de Linux en la línea de comandos de Windows y viceversa.
- **Sin Necesidad de Máquina Virtual:**
  - A diferencia de las máquinas virtuales tradicionales, WSL no requiere una máquina virtual separada. Utiliza una tecnología de traducción de llamadas de sistema para integrar los entornos.
- **Soporte para Desarrollo:**
  - WSL es especialmente útil para desarrolladores que trabajan en entornos mixtos. Permite usar herramientas y utilidades de desarrollo de Linux junto con las herramientas de desarrollo de Windows.
- **Versiones de WSL:**
  - Hasta mi última actualización en enero de 2022, WSL tenía dos versiones principales: WSL 1 y WSL 2. WSL 1 utiliza una traducción de llamadas de sistema, mientras que WSL 2 utiliza una máquina virtual ligera para ofrecer mejor rendimiento y compatibilidad.
- **Docker en WSL 2:**
  - WSL 2 es especialmente popular entre los desarrolladores porque mejora la compatibilidad con Docker. Puedes ejecutar contenedores Docker directamente en el entorno WSL 2.





## Instalación en Windows:

Para iniciar la instalación del WSL hemos de seguir la documentación oficial de 

[Windows]: https://learn.microsoft.com/es-es/windows/wsl/install

 
