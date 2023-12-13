# Docker

## Información general

- Plataforma de código abierto que facilita la creación, implementación y ejecución de aplicaciones mediante contenedores.
- Permite empaquetar una aplicación y sus dependencias en un contenedor virtual que se puede ejecutar en cualquier entorno.
- Utiliza características del kernel del sistema operativo, como cgroups y namespaces, para crear entornos aislados.
- Las imágenes son capas de solo lectura.
- Los contenedores añaden una capa de escritura encima de la imagen base para realizar cambios.
- **Arquitectura**
- **Docker Engine**: Componente central que gestiona los contenedores y su ejecución.
- **Docker Images**: Plantillas de solo lectura que contienen el sistema operativo, aplicaciones y dependencias.
- **Docker Containers**: Instancias en tiempo de ejecución de imágenes. Son entornos aislados donde se ejecutan las aplicaciones.

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20221205115118/Architecture-of-Docker.png"/>
</p>

- **Contenedor**
- Un entorno ligero y portátil que contiene todo lo necesario para ejecutar una aplicación: código, bibliotecas, herramientas y configuraciones.
- Se ejecutan sobre un único sistema operativo anfitrión y comparten el mismo kernel del sistema, pero están aislados entre sí.

- **Comandos básicos**:

| Comando                                                      | Descripción                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `docker pull <imagen>`| Descarga una imagen desde Docker Hub u otro registro |
| `docker run <imagen>`  | Crea y ejecuta un contenedor basado en una imagen |
| `docker ps`   | Muestra los contenedores en ejecución |
| `docker stop <contenedor>`  | Detiene un contenedor en ejecución |
| `docker rm <contenedor>` | Elimina un contenedor |
| `docker rmi <imagen>` | Elimina una imagen localmente |
| `docker build <ruta>`  | Crea una imagen a partir de un Dockerfile en una ruta específica |


## Docker images

- Una imagen es una plantilla de solo lectura utilizada para crear contenedores.
- Contiene todo lo necesario para ejecutar una aplicación: código, bibliotecas, herramientas, archivos y configuraciones.
- Las imágenes se componen de una serie de capas superpuestas y son la base sobre la cual se crean los contenedores.
- **Registros de Docker**
- Son repositorios que almacenan y distribuyen imágenes de Docker.
- El **Docker Hub** es el registro público más utilizado, pero también se pueden configurar registros privados.
- Los usuarios pueden buscar, descargar, cargar y compartir imágenes a través de estos registros.
- **Imagenes**
- Se construyen a partir de un archivo llamado **Dockerfile** que contiene instrucciones paso a paso para crear la imagen.
- Las instrucciones pueden incluir la instalación de paquetes, la configuración del entorno, la copia de archivos y la definición de comandos a ejecutar al iniciar el contenedor.
- Las imágenes en Docker están compuestas por múltiples capas. Cada capa representa un cambio o adición al sistema de archivos.
- Las capas son de solo lectura y se superponen para formar la imagen final.
 
<p align="center">
  <img src="https://lh6.googleusercontent.com/H8mhf23JNy-zCPrLaNs_H4h6K1xLRHv-P0JS4_Ad86xSo7En4tLT3POuOJPrcBNXG5lWDy2Y6fdNzRrzoB9SSLxrHhwrdk-qO28__D19NzO01OkkyBdr7YzZo2K_46HidAoUpmxeW2FOF42uOtAg3Pnfe_gcWafYs7xYywgdFeRdK3kV-p7LfIY7Z9h9tg"/>
</p>

- **Administración imágenes**:

| Comando                                                      | Descripción                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `docker pull <imagen>`| Descarga una imagen desde Docker Hub u otro registro |
| `docker images`  | Lista todas las imágenes almacenadas localmente |
| `docker rmi <imagen>` | Elimina una imagen localmente |
| `docker history <imagen>`   | Muestra el historial de capas de una imagen |
| `docker save <imagen> y docker load <archivo.tar>`  | Guarda y carga imágenes en un archivo comprimido .tar |

- **Buenas prácticas**
- Priorizar las imágenes provenientes de fuentes confiables y oficiales, como el Docker Hub oficial.
- Eliminar elementos innecesarios, usar imágenes base más ligeras y optimizar el Dockerfile para reducir el tamaño final de la imagen.
- Etiquetar las imágenes con versiones claras y significativas para facilitar su gestión y control.
- Escanear las imágenes en busca de vulnerabilidades utilizando herramientas de seguridad específicas para Docker.

## Docker Persistent Storage

- Permite que los datos sobrevivan al ciclo de vida de los contenedores. Esto es crucial para aplicaciones que requieren almacenamiento persistente.
- Facilita la migración de contenedores con datos entre diferentes entornos sin perder información.
- Permite que múltiples contenedores accedan y compartan datos almacenados en volúmenes.
- **casos de uso**
- **Bases de datos**: Permiten almacenar datos de aplicaciones de base de datos de forma persistente fuera del contenedor.
- **Archivos de configuración**: Almacenamiento de archivos de configuración que necesitan persistir entre diferentes versiones del contenedor.
- **Logs y registros**: Persistencia de registros generados por aplicaciones para su posterior análisis.
- **Tipos de almacenamiento persistente**
- **Volúmenes**: Son directorios especiales gestionados por Docker y que existen fuera del sistema de archivos del contenedor. Pueden ser compartidos entre varios contenedores.
- **Bind Mounts**: Enlazan un directorio o archivo específico del sistema anfitrión al contenedor. Los datos están directamente disponibles en el sistema anfitrión y pueden ser accedidos por el contenedor.

- **Gesitón de volúmenes**

| Comando                                                      | Descripción                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `docker volume create <nombre>`| Crea un nuevo volumen |
| `docker volume ls`  | Lista todos los volúmenes disponibles |
| `docker volume rm <nombre>` | Elimina un volumen |
| `docker volume inspect <nombre>`   | Muestra información detallada sobre un volumen específico |

- **Buenas prácticas**
- Utilizar volúmenes para datos críticos: Para garantizar la persistencia de datos importantes, especialmente en entornos de producción.
- Documentar y versionar volúmenes y montajes de enlace: Para facilitar la gestión y replicación del entorno.
- Asegurar permisos de acceso: Asegurarse de que los permisos de acceso a los volúmenes y montajes de enlace sean adecuados para garantizar la seguridad de los datos.

## Dockerfile

- Es un archivo de texto plano que contiene una lista de instrucciones detalladas sobre cómo construir una imagen de Docker paso a paso.
- Estas instrucciones describen los pasos necesarios para configurar el entorno dentro del contenedor.
- `docker build -t <nombre_imagen>:<tag> <ruta_directorio>`: Construye una imagen a partir de un Dockerfile en un directorio específico y le asigna un nombre y etiqueta.
  
- **Estructura básica**

| Instrucción                                                  | Descripción                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `FROM`| Especifica la imagen base desde la cual se construirá la nueva imagen |
| `RUN`  | Ejecuta comandos dentro del contenedor durante el proceso de construcción de la imagen |
| `COPY y ADD` | Copian archivos del sistema local al sistema del contenedor durante la construcción de la imagen |
| `ENV`   |  Establece variables de entorno dentro del contenedor |
| `WORKDIR` | Establece el directorio de trabajo para los comandos siguientes en el Dockerfile |

- **Mejores prácticas**
- Minimizar capas: Agrupar comandos RUN para reducir el número de capas en la imagen final y minimizar su tamaño.
- Usar imágenes base oficiales y ligeras: Preferir imágenes base oficiales y más ligeras para reducir el tamaño de la imagen resultante.
- Eliminar archivos temporales: Limpiar archivos temporales y cachés después de ejecutar comandos para reducir el tamaño de la imagen.
- Utilizar **.dockerignore**: Ignorar archivos y directorios no necesarios en el contexto de construcción para evitar que se incluyan en la imagen.
  
- **Ejemplo Dockerfile**
  
```
# Utilizamos una imagen base de Ubuntu 20.04
FROM ubuntu:20.04

# Actualizamos los repositorios e instalamos Python 3
RUN apt-get update && apt-get install -y python3

# Establecemos el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiamos los archivos locales al directorio /app del contenedor
COPY . /app

# Ejecutamos un comando al iniciar el contenedor (por ejemplo, iniciar una aplicación Python)
CMD ["python3", "app.py"]
```

