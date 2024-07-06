# Blue Team

## Filter Captures in Wireshark

- Wireshark es un potente analizador de protocolos de red.
- Permite capturar e inspeccionar los datos que viajan de un lado a otro en una red.
- Para filtrar capturas en Wireshark y obtener información muy detallada, puedes utilizar filtros de visualización.
- Estos filtros te ayudarán a centrarte en paquetes específicos o tipos de tráfico.
- Capturar solo los paquetes relevantes, conservando el espacio en disco y el tiempo de análisis.
- **Filtros de visualización comunes**
  + `ip.addr == X.X.X.X`: Este filtro muestra paquetes con una dirección IP de origen o destino de X.X.X.X.
  + `tcp.port == 80`: Muestra paquetes con un puerto de origen o destino de 80 (HTTP).
  + `dns`: Muestra solo el tráfico DNS.
  + `http`: Muestra solo el tráfico HTTP.
  + `frame.number <= 100`: Limita la visualización a los primeros 100 frames capturados.
- Puedes utilizar operadores lógicos (and, or, not) para combinar múltiples condiciones.

## Process Monitor (ProcMon)

- Es una herramienta que se utiliza para supervisar el sistema de archivos, el registro y la actividad en tiempo real.
- Herramienta poderosa para solucionar problemas, diagnosticar problemas y detectar malware.
- Captura una amplia gama de eventos, incluyendo accesos al sistema de archivos, cambios en el registro, creación y finalización de procesos y subprocesos.
- Utilizar ProcMon para capturar datos mientras se ejecuta un programa sospechoso.
- ProcMon también puede utilizarse para identificar las técnicas que utilizan los malware para propagarse o evadir la detección.
- ProcMon facilita la detección de comportamientos maliciosos, como la modificación no autorizada de archivos, la manipulación del registro del sistema o la comunicación sospechosa a través de la red.
- Sirve como una herramienta invaluable en el análisis forense de sistemas comprometidos.

<p align="center">
  <img src="https://learn.microsoft.com/en-us/sysinternals/downloads/media/procmon/procmon-main.png"/>
</p>

## Windows Registry Introduction and Structure

- El registro de Windows es una base de datos jerárquica que contiene datos críticos para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows.
- Los datos se estructuran en un formato de árbol, con cada nodo del árbol denominado clave.
- Cada clave puede contener subclaves y entradas de datos denominadas valores.
- Configuración del sistema, como la ubicación de la carpeta de inicio, la pantalla de inicio de sesión y las preferencias de energía.
- Configuración de las aplicaciones, como los accesos directos, las preferencias y las opciones de seguridad.
- Configuración de los servicios, como los servicios de red y los servicios de impresión.
- El Registry Editor es una herramienta de Windows que permite ver y editar el registro.
- Se puede utilizar para realizar cambios en la configuración del sistema, las aplicaciones y los servicios.
- Los atacantes pueden utilizar el registro para instalar malware, robar información o causar daños al sistema.

<p align="center">
  <img src="https://www.bleepstatic.com/images/news/tutorials/windows/r/how-to-use-registry-editor/windows-registry-editor.jpg"/>
</p>

## Recycle Bin Forensic and Rifiuti2 Tool

- La papelera de reciclaje es una carpeta especial en un sistema operativo que almacena los archivos y carpetas que han sido eliminados.
- Cuando un usuario elimina un archivo o carpeta, el sistema operativo no lo elimina de forma permanente, sino que lo mueve a la papelera de reciclaje.
- La papelera de reciclaje proporciona una forma de recuperar archivos y carpetas que han sido eliminados accidentalmente.
- También se puede utilizar para archivar archivos que no se necesitan en el disco duro principal.
- **Rifiuti2**
  + Es una herramienta de código abierto que se utiliza para analizar la Papelera de reciclaje en sistemas informáticos Windows.
  + La herramienta es capaz de recuperar datos eliminados de la Papelera de reciclaje de Windows 95 a Windows 10.
  + Funciona analizando los archivos INFO2 y INFO3 que se encuentran en la Papelera de reciclaje.
  + Estos archivos contienen información sobre los archivos eliminados, como la hora y la fecha de eliminación, la ruta original del archivo y el tamaño del archivo.
  + Puede utilizarse para recuperar pruebas de delitos informáticos, como archivos de imágenes o documentos que hayan sido eliminados por un sospechoso.
    
## Introduction to Prefetch Files

- Son archivos creados por el sistema operativo Windows cada vez que se ejecuta una aplicación por primera vez.
- Estos archivos contienen información sobre los recursos que se utilizaron para cargar la aplicación, como los archivos DLL, los archivos de iconos y los archivos de datos.
- Se utilizan para acelerar el inicio de las aplicaciones.
- Cuando Windows se inicia, carga los Prefetch Files para las aplicaciones que se utilizan con frecuencia.
- Esto permite que Windows cargue las aplicaciones más rápido, ya que no tiene que buscar los recursos necesarios en el disco duro.
- Prefetch Files de aplicaciones: Estos archivos se crean para cada aplicación que se ejecuta por primera vez.
- Prefetch Files de servicios: Estos archivos se crean para cada servicio que se inicia en Windows.
- **PECmd**
  + Es una herramienta de línea de comandos que se puede utilizar para administrar los Prefetch Files.
  + Listar todos los Prefetch Files: `PECmd /list`
  + Listar los Prefetch Files de una aplicación específica: `PECmd /list "c:\windows\system32\calc.exe"`
  + Eliminar todos los Prefetch Files: `PECmd /delete`
  
## Introduction to Sysmon Sysinternals

- Es una herramienta gratuita de Microsoft que proporciona supervisión y registro detallados de la actividad del sistema en Windows.
- Se trata de un servicio del sistema y un controlador de dispositivo que se instala en el sistema y permanece residente a través de los reinicios del sistema.
- Sysmon se puede instalar y configurar utilizando la herramienta Sysmon Configuration Utility.
- Esta herramienta permite seleccionar los eventos que se van a registrar y personalizar los parámetros de registro.
- Es una herramienta esencial para cualquier administrador de sistemas que desee proteger su sistema contra amenazas.
- Sysmon puede utilizarse para detectar una amplia gama de actividades sospechosas
  + Inicio de procesos desde ubicaciones no autorizadas.
  + Creación de procesos con líneas de comandos sospechosas.
  + Conexiones de red a destinos no autorizados.
  + Cambios en la hora de creación de archivos.
  
## Introduction to Autopsy

- Autopsy es un software forense de código abierto que se utiliza para analizar datos digitales.
- Análisis de datos de múltiples fuentes: puede analizar datos de una variedad de fuentes, incluyendo discos duros, unidades USB, tarjetas SD, dispositivos móviles, correo electrónico, archivos de registro y más.
- Visualización de datos: proporciona una variedad de herramientas para visualizar datos, lo que facilita la identificación de patrones y anomalías.
- Extracción de datos: puede extraer datos de fuentes digitales, lo que los hace disponibles para su análisis más detallado.
- Reportes: puede generar informes detallados de los resultados del análisis.
- **Comandos comunes**
  + `autopsy`: Inicia Autopsy.
  + `autopsy -case <nombre_del_caso>`: Abre un caso existente.
  + `autopsy -add-source <ruta_de_la_fuente_de_datos>`: Agrega una fuente de datos a un caso.
  + `autopsy -analyze`: Analiza un caso.
  + `autopsy -report`: Genera un informe de un caso.
 
## Introduction to Memory Forensics

- Es una rama de la forense digital que se centra en el análisis de la memoria de un sistema informático.
- La memoria es un componente fundamental de cualquier sistema informático, ya que almacena los datos que están en uso en ese momento.
- Puede proporcionar información valiosa sobre las actividades que se han llevado a cabo en un sistema informático, incluso si se han eliminado los datos del disco duro.
- Investigación de incidentes de seguridad: puede utilizarse para investigar incidentes de seguridad, como ataques de malware o intrusiones en sistemas.
- Recuperación de datos: puede utilizarse para recuperar datos que han sido eliminados o cifrados.
- Datos en uso: La memoria contiene los datos que están en uso en ese momento, como los archivos abiertos, las variables de proceso y los datos de la pila.
- Datos de proceso: La memoria contiene datos sobre los procesos que se están ejecutando en el sistema, como los nombres de los procesos, los PID y los argumentos de la línea de comandos.
- Datos de sistema: La memoria contiene datos sobre el sistema operativo y el hardware, como la configuración del sistema, los controladores de dispositivos y los registros de eventos.
- **Herramientas**
  + FTK Imager: FTK Imager es una herramienta gratuita y de código abierto que se utiliza para adquirir imágenes de memoria.
  + Volatility: Volatility es una herramienta gratuita y de código abierto que se utiliza para analizar imágenes de memoria.
  + X-Ways Forensics: X-Ways Forensics es una herramienta comercial que ofrece una amplia gama de funciones para la forense de memoria.
  
## Memory Forensics using Volatility

- Volatility Framework es una herramienta de código abierto para análisis forense de memoria.
- Es una herramienta poderosa que se puede utilizar para recopilar información valiosa de una imagen de memoria, como procesos en ejecución, archivos, network connections y más.
- Volatility está disponible para Windows, Linux, macOS, y Android.
- Está escrito en Python y se puede ejecutar en cualquier sistema operativo que tenga Python instalado.
- **Comandos comunes**
  + `pslist`: Lista todos los procesos en ejecución en el momento de la captura de memoria.
  + `pstree`: Muestra un árbol de procesos de todos los procesos en ejecución.
  + `psscan`: Busca procesos que coincidan con un criterio específico, como el nombre del proceso o el PID.
  + `yarascan`: Busca firmas de malware en la memoria.
  + `memdump`: Extrae un archivo de memoria de una imagen de memoria.
  + `dllist`: Lista todos los módulos cargados en la memoria.
  + `ldrmodules`: Lista todos los módulos cargados en la memoria, junto con su ubicación en el disco.
  + `prviw`: Muestra una vista previa de un archivo de la memoria.
  + `cmdline`: Lista los comandos que se han ejecutado en el sistema.
  + Listar todos los procesos en ejecución: `volatility -f memory.dmp pslist`
  + Listar todos los módulos cargados en la memoria: `volatility -f memory.dmp dllist`
  + Listar todos los archivos abiertos: `volatility -f memory.dmp filescan`
  + Recuperar información de cuentas: `volatility -f memory.dmp printkey -k SAM`
  + Escanear una imagen de memoria en busca de conexiones de red: `volatility -f memory.dmp netscan -t TCP`
  + Enumerar todas las claves del registro que se encuentran en una imagen de memoria: `volatility -f memory.dmp hivelist`
- **Recuperar información de cuentas**
  + Volatility puede utilizarse para recuperar información de cuentas como nombres de usuario, contraseñas, y políticas de contraseñas.
  + Para recuperar información de cuentas, se puede utilizar el comando printkey. Este comando permite imprimir el contenido de una clave del registro.
  + `volatility -f memory.dmp printkey -k SAM`
  + El output del comando anterior incluye el siguiente:
  ```
  sam\Domains\Account\Names\0000000000000000
  sam\Domains\Account\Names\0000000000000001
  ...
  sam\Domains\Account\Names\00000000ffffffff
  ```
  + Cada línea del output representa una cuenta de usuario. La información de cada cuenta incluye el siguiente: El nombre de usuario, el SID de la cuenta, el tipo de cuenta, el estado de la cuenta.
  + También se puede utilizar el comando pslist para recuperar información de cuentas.
  + Este comando lista todos los procesos en ejecución en el momento de la captura de memoria.
  + Para cada proceso, el comando pslist muestra el nombre del proceso, el PID, y la imagen base del proceso.
  + Para recuperar información de cuentas de un proceso específico, se puede utilizar el comando printkey junto con el argumento -p.
  + Este argumento especifica el PID del proceso.
  + `volatility -f memory.dmp printkey -k SAM -p 12345`: imprime el contenido de la clave SAM del proceso con el PID 12345
- Conexiones de red
  + El comando netscan se utiliza para escanear una imagen de memoria en busca de conexiones de red.
  + El output del comando netscan incluye el siguiente: el tipo de conexión (TCP, UDP, etc.), el estado de la conexión (establecida, cerrada, etc.), la dirección IP local, el puerto local, la dirección IP remota, el puerto remoto.
  + `volatility -f memory.dmp netscan -t TCP`: escaneará una imagen de memoria en busca de conexiones TCP
