# Dockers fundamentals

Bienvenidos a la guía básica, para principiantes, sobre dockers realizada por Ramon Peinado Ruiz gracias al .

## CONCEPTOS BASICOS

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



### Comandos básicos:

Aquí tienes un resumen de algunos comandos básicos de Docker que te serán útiles:

1. **`docker pull`:**

   Descarga una imagen de Docker desde un registro (por defecto, Docker Hub).

   ```
   docker pull nombre_de_la_imagen
   ```

2. **`docker run`:**

   Crea y ejecuta un contenedor a partir de una imagen.

   ```
   docker run nombre_de_la_imagen
   ```

3. **`docker ps`:**

   Muestra los contenedores en ejecución.

   ```
   docker ps
   ```

4. **`docker ps -a`:**

   Muestra todos los contenedores, incluso los que no están en ejecución.

   ```
   docker ps -a
   ```

5. **`docker stop`:**

   Detiene un contenedor en ejecución.

   ```
   docker stop ID_del_contenedor
   ```

6. **`docker rm`:**

   Elimina un contenedor.

   ```
   docker rm ID_del_contenedo
   ```

7. **`docker images` o `docker image ls`:**

   Muestra las imágenes descargadas en la máquina.

   ```
   docker images
   ```

8. **`docker rmi`:**

   Elimina una imagen de Docker.

   ```
   docker rmi nombre_de_la_imagen
   ```

9. **`docker exec`:**

   Ejecuta un comando en un contenedor en ejecución.

   ```
   docker exec ID_del_contenedor comando
   ```

10. **`docker build`:**

    Construye una imagen a partir de un Dockerfile.

    ```
    docker build -t nombre_de_la_imagen ruta_del_Dockerfile
    ```

11. **`docker-compose`:**

    Gestiona aplicaciones multi-contenedor utilizando un archivo YAML (docker-compose.yml) para definir la configuración.

    ```
    docker-compose up
    ```

12. **`docker logs`:**

    Muestra los logs de un contenedor en ejecución.

    ```
    docker logs ID_del_contenedor
    ```

13. **`docker-compose down`:**

    Detiene y elimina todos los servicios y contenedores definidos en el archivo `docker-compose.yml`. También puede eliminar las redes y volúmenes asociados.

    ```
    docker-compose down
    ```

14. **`docker container top`:**

    Este comando se utiliza para mostrar los procesos que se están ejecutando dentro de un contenedor específico. Proporciona una visión de los procesos activos dentro del espacio de nombres del contenedor, similar a la salida del comando `top` en sistemas Linux

    ```
    docker container top nombre_del_contenedor
    ```

15. **`docker container inspect`:**

    Se utiliza para obtener información detallada sobre un contenedor. Proporciona un formato JSON con detalles sobre la configuración, redes, volúmenes, variables de entorno y más.

    ```
    docker container inspect nombre_del_contenedor
    ```

16. **`docker container stats`:**

    Este comando muestra estadísticas en tiempo real sobre el uso de recursos del contenedor, como CPU, memoria y redes. Proporciona una interfaz de estilo "top" para monitorear el rendimiento del contenedor

    ```
    docker container stats nombre_del_contenedor
    ```

17. **`docker-compose down`:**

    Detiene y elimina todos los servicios y contenedores definidos en el archivo `docker-compose.yml`. También puede eliminar las redes y volúmenes asociados.

    ```
    docker-compose down
    ```

18. **`docker container run -it`:**

    Este comando inicia un contenedor de forma interactiva, lo que significa que te conectas directamente a la consola del contenedor. El flag `-it` combina dos opciones:
    - `-i` o `--interactive`: Mantiene abierta la entrada estándar del contenedor.
    - `-t` o `--tty`: Asocia un seudoterminal (TTY) para permitir la interacción.

    ```
    docker container run -it nombre_de_la_imagen
    ```

19. **`docker container exec -it`:**

    Este comando se utiliza para ejecutar un comando adicional en un contenedor que ya está en ejecución. El flag `-it` se utiliza de manera similar al comando `docker container run`..

    ```
    docker container exec -it nombre_del_contenedor comando_adicional
    ```

20. **`docker container run --help`:**

    Este comando muestra la ayuda y documentación relacionada con el comando `docker container run`. Proporciona información sobre las opciones disponibles y la sintaxis del comando.

    ```
    docker container run --help
    ```

21. **`docker run --rm`:**

    Este comando crea y ejecuta un contenedor a partir de una imagen. El flag `--rm` asegura que el contenedor se elimine automáticamente una vez que se detenga.

    ```
    docker run --rm nombre_de_la_imagen
    ```



### Imágenes

Una imagen es la aplicación que queremos ejecutar como una ISO, un contenedor es la instancia de esa imagen corriendo, se pueden tener muchos contenedores de la misma imagen corriendo

Algunas de las imágenes disponibles en Docker mas conocidas, ampliamente usadas y como obtenerlas:

**Ubuntu:**

La imagen oficial de Ubuntu proporciona un sistema base Ubuntu que se utiliza comúnmente para aplicaciones que requieren un entorno Linux.

```bash
docker pull ubuntu
```

**Alpine Linux:**

Alpine Linux es conocida por ser una distribución Linux muy ligera y segura, lo que la hace popular en entornos de contenedores.

```bash
docker pull alpine
```

**Nginx:**

La imagen oficial de Nginx se utiliza para ejecutar servidores web basados en el servidor Nginx.

```bash
docker pull nginx
```

**Node.js:**

La imagen oficial de Node.js es esencial para desarrolladores de JavaScript que desean ejecutar aplicaciones Node.js en contenedores.

```bash
docker pull node
```

**MySQL:**

La imagen oficial de MySQL se utiliza para ejecutar servidores de bases de datos MySQL en contenedores.

```bash
docker pull mysql
```

**PostgreSQL:**

Similar a MySQL, la imagen oficial de PostgreSQL es utilizada para ejecutar servidores de bases de datos PostgreSQL.

```bash
docker pull postgres
```

**MongoDB:**

La imagen oficial de MongoDB se utiliza para ejecutar servidores de bases de datos MongoDB en contenedores.

```bash
docker pull mongo
```

**Redis:**

La imagen oficial de Redis se utiliza para ejecutar servidores de almacenamiento en caché y bases de datos en memoria.

```bash
docker pull redis
```

**Python:**

La imagen oficial de Python es esencial para desarrolladores de Python que desean ejecutar aplicaciones Python en contenedores.

```bash
docker pull python
```

**Microsoft .NET Core:**

Para desarrolladores que trabajan con aplicaciones basadas en .NET Core, la imagen oficial de Microsoft .NET Core es clave.

```bash
docker pull mcr.microsoft.com/dotnet/core/runtime
```

### WSL o Windows Subsystem for linux:

Es una característica de Windows que permite ejecutar un entorno Linux directamente en un sistema operativo Windows. Básicamente, WSL proporciona una capa de compatibilidad que permite a los usuarios de Windows ejecutar binarios de Linux de forma nativa.

Ventajas y caracteristicas:

- **Entorno Linux en Windows:**
  
  WSL permite ejecutar distribuciones de Linux, como Ubuntu, Debian y otras, directamente en un sistema Windows sin la necesidad de una máquina virtual.
- **Interoperabilidad:**
  
  Facilita la interoperabilidad entre aplicaciones y herramientas diseñadas para Linux y el entorno Windows. Puedes ejecutar comandos de Linux en la línea de comandos de Windows y viceversa.
- **Sin Necesidad de Máquina Virtual:**
  
  A diferencia de las máquinas virtuales tradicionales, WSL no requiere una máquina virtual separada. Utiliza una tecnología de traducción de llamadas de sistema para integrar los entornos.
- **Soporte para Desarrollo:**
  
  WSL es especialmente útil para desarrolladores que trabajan en entornos mixtos. Permite usar herramientas y utilidades de desarrollo de Linux junto con las herramientas de desarrollo de Windows.
- **Versiones de WSL:**
  
  Hasta mi última actualización en enero de 2022, WSL tenía dos versiones principales: WSL 1 y WSL 2. WSL 1 utiliza una traducción de llamadas de sistema, mientras que WSL 2 utiliza una máquina virtual ligera para ofrecer mejor rendimiento y compatibilidad.
- **Docker en WSL 2:**
  
  WSL 2 es especialmente popular entre los desarrolladores porque mejora la compatibilidad con Docker. Puedes ejecutar contenedores Docker directamente en el entorno WSL 2.



## Instalación en Windows:

Para iniciar la instalación del WSL hemos de seguir la documentación oficial de Windows (https://learn.microsoft.com/es-es/windows/wsl/install)

Iniciamos nuestro PowerShell o nuestro símbolo del sistema como administrador ejecutamos el siguiente comando y reiniciamos nuestro equipo:

```powershell
wsl --install
```

Después de esto vamos al market store de Windows y seleccionamos la distribución de Linux con la que queramos trabajar, nosotros vamos a trabajar con Ubuntu 22.04.2 LTS (https://apps.microsoft.com/detail/9PN20MSR04DW?gl=ES&hl=es-es) y con AlmaLinux9: (https://apps.microsoft.com/detail/9P5RWLM70SN9?gl=US&hl=en-us)

Nos descargamos Docker para Windows (https://docs.docker.com/desktop/install/windows-install/) e iniciamos el ejecutable, se recomienda reiniciar el equipo de nuevo.

Una vez realizada la instalación p**odremos abrir nuestro Ubuntu** de manera sencilla, cabe recordar que si a la hora de la configuracion se nos pide una contraseña es **MUY** importante no olvidarla ya que nos servirá para ejecutar comandos en modo root.

<img align="center" src="/img/2ºimagenn.PNG"  />

## Creando nuestra primera imagen en un contenedor

Vamos a crear nuestra primera imagen de NGINX, nginx es un servidor proxy inverso de código abierto para los protocolos HTTP, HTTPS, SMTP, POP3 e IMAP, así como un equilibrador de carga, caché HTTP y un servidor web (servidor de origen). El proyecto nginx comenzó con un fuerte enfoque en alta concurrencia, alto rendimiento y bajo uso de memoria. Está bajo la licencia BSD de 2 cláusulas y se ejecuta en Linux, variantes de BSD, Mac OS X, Solaris, AIX, HP-UX, así como en otras variantes de *nix. También tiene una versión de prueba para Microsoft Windows.



Para saber como crear la imagen de NGINX es tan facil como buscar en la documentación oficial de Docker (https://hub.docker.com/_/nginx)



Buscamos en la parte donde ponga Exposing external port o Exponiendo el puerto externo, asi podemos comprobar accediendo a http://localhost:8080 que la imagen esta funcionando correctamente

```bash
docker container run --publish 80:80 nginx
```

Si al ejecutar el comando nos genera el siguiente error:

<img align="center" src="/img/3ºimagenn.PNG"  />

Puede ser por que Docker Desktop no este en funcionamiento o por que no tenemos la opcion de Usar motor basado en WSL 2 en cuyo caso

Accedemos a la siguiente pagina https://docs.docker.com/desktop/wsl/:



Este comando hace lo siguiente:

▪ Se descarga una imagen de nginx de Docker Hub.
▪ Inicia un nuevo contenedor para esa imagen.
▪ Abre el puerto 80 en la máquina Linux.
▪ Enruta el tráfico del puerto escogido, al puerto 80 del contenedor.

Si comprobamos yendo a localhost veremos algo así:

<img align="center" src="/img/4ºimagenn.PNG"  />

Para dejarlo corriendo en segundo plano pulsamos` ctrl + c` si quisiésemos inicializarlo desde el inicio en segundo plano ejecutaremos:

```bash
docker container run --publish 80:80 --detach nginx
```

Que responderá con un ID unico:

<img align="center" src="/img/5ºimagenn.PNG"  />





## EJERCICIO INFORMACION PERSISTENTE

<img align="center" src="/img/6ºimagenn.PNG"  />













## EJERCICIO DOCKER COMPOSE Y YAML

<img align="center" src="/img/7ºimagenn.PNG"  />









 
