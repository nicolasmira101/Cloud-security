# Vulnerabilidades

## Follina

- Vulnerabilidad de dia cero de Microsoft.
- Afecta a la herramienta Microsoft Windows Support Diagnostic Tool (MSDT).
- MSDT es una herramienta de diagnóstico que se utiliza para recopilar información sobre el sistema del usuario.
- Se relaciona con la manipulación incorrecta de ciertos objetos en la memoria de un sistema.
- La explotación exitosa de esta vulnerabilidad podría permitir a un atacante ejecutar código malicioso en el sistema afectado.
- CVE-2022-30190.
- Desactivar la ejecución automática de macros en Microsoft Office.

## Microsoft MSHTML

- Vulnerabilidad de ejecución remota de código (RCE) en el componente MSHTML de Microsoft Windows.
- Permite a un atacante ejecutar código arbitrario en el sistema vulnerable con los privilegios del usuario que abrió el documento malicioso.
- Se puede explotar mediante documentos de Microsoft Office que contienen un control ActiveX malicioso.
- La vulnerabilidad se encuentra en el componente MSHTML, que es el motor de renderizado web de Internet Explorer.
- La vulnerabilidad se produce cuando MSHTML intenta procesar un control ActiveX malicioso.

## Log4Shell

- Vulnerabilidad de ejecución remota de código (RCE) en la biblioteca de registro de Java, Log4j.
- Permite a un atacante ejecutar código arbitrario en un sistema vulnerable.
- Fue reportada a Apache el 24 de noviembre de 2021 y publicada públicamente el 9 de diciembre de 2021.
- Log4j utiliza una función llamada JNDI (Java Naming and Directory Interface) para buscar información en un directorio remoto.
- La vulnerabilidad permite a un atacante inyectar código maliciosos en el mensaje de registro.
- Cuando Log4j intenta resolver la referencia JNDI, ejecuta el código malicioso en el sistema vulnerable.
- Una de las vulnerabilidades de seguridad más graves de la historia.
- Afectó a millones de sistemas en todo el mundo.
- Se utilizó para realizar ataques a organizaciones gubernamentales, empresas y particulares.
- Es importante actualizar todos los sistemas que utilicen Log4j a la versión más reciente.
- Deshabilitar la función JNDI.
- Utilizar un firewall para bloquear el tráfico JNDI.

## PrintNightmare

- Es una vulnerabilidad de RCE que afecta al servicio de cola de impresión de Windows (Spooler).
- Un atacante podría ejecutar código arbitrario con privilegios de SYSTEM en un sistema afectado.
- Afecta a todas las versiones de Windows desde Windows 7 hasta Windows 11, incluidas las versiones de servidor.
- La vulnerabilidad se puede explotar enviando un archivo de impresión malicioso a un sistema afectado.
- El archivo de impresión malicioso se abrirá automáticamente por el servicio Spooler y ejecutará el código malicioso.
- Microsoft lanzó un parche para esta vulnerabilidad el 13 de julio de 2021.
- CVE-2021-34527

## MPI Desynchronization

- Es una condición de carrera que puede ocurrir en aplicaciones que utilizan el protocolo de comunicación MPI.
- Se produce cuando dos procesos MPI acceden a la misma variable compartida en el mismo momento.
- Un atacante puede aprovechar esta vulnerabilidad para tomar el control de un sistema remoto.

## 7-Zip Zero-Day

- Vulnerabilidad de ejecución remota de código (RCE) en la biblioteca de compresión 7zip.
- Permite a un atacante ejecutar código arbitrario en el sistema de un usuario vulnerable.
- Error en el manejo de memoria durante la descompresión de archivos RAR.
- Un atacante puede enviar un archivo RAR malicioso a una víctima.
- Cuando la víctima abre el archivo, el exploit se ejecuta y permite al atacante tomar el control del sistema.
- CVE-2022-29072.
- La vulnerabilidad se encuentra en la función `ExtractFile` de la biblioteca 7zip.
- El error ocurre cuando la función intenta abrir un archivo que contiene un nombre de archivo con caracteres especiales.
- el exploit puede modificar la dirección de memoria de la función ExtractFile para que apunte a un código malicioso.
- La vulnerabilidad se ha corregido en la versión 19.00 de 7zip 

## Spectre Vulnerability

- Es una vulnerabilidad que afecta a los microprocesadores modernos que utilizan predicción de saltos.
- Puede permitir a un atacante robar información confidencial, como contraseñas, datos bancarios o secretos comerciales.
- Los microprocesadores modernos utilizan una técnica llamada predicción de saltos para acelerar el rendimiento.
- La predicción de saltos consiste en que el procesador intenta predecir a qué dirección de memoria se dirigirá el siguiente salto de código.
- Si la predicción es correcta, el procesador puede empezar a ejecutar el código de la siguiente dirección antes de que el salto se haya completado.
- Sin embargo, si la predicción es incorrecta, el procesador debe descartar el código especulativo que ya ha ejecutado.
- Los ataques Spectre se basan en la capacidad de un atacante para observar los efectos colaterales de la ejecución especulativa.
- Un atacante puede observar el tiempo que tarda en cargarse una dirección de memoria para determinar si contiene información confidencial.
- Los fabricantes de procesadores han lanzado actualizaciones de microcódigo que reducen el riesgo de ataques Spectre.
- Spectre podía ser utilizado para robar contraseñas de Windows.

## Nimbuspwn

- Un grupo de vulnerabilidades de escalada de privilegios en Linux que podrían permitir a un atacante elevar los privilegios a root en muchos puntos finales de escritorio de Linux.
- CVE-2022-29799 y CVE-2022-29800
-  Las vulnerabilidades se pueden explotar mediante la creación de un script malicioso que se ejecuta cuando cambia el estado de la conexión de red.
-  CVE-2022-29799: Vulnerabilidad de recorrido de directorio y de enlace simbólico. Un atacante podría generar su propio estado y redirigir la llamada "networkd-dispatcher" a otro directorio.
-  CVE-2022-29800: Vulnerabilidad de condición de carrera de tiempo de comprobación y tiempo de uso (TOCTOU). Un atacante podría aprovechar el tiempo entre el descubrimiento y ejecución de los scripts para reemplazar los scripts por otros que "networkd-dispatcher" cree que son propiedad de root.
  
## Uber Ride with Teapot

- Permitía a un atacante realizar un ataque de denegación de servicio (DoS) a la aplicación Uber.
- El atacante enviaba una solicitud HTTP a la aplicación Uber con un encabezado específico que hacía que la aplicación generara una respuesta de gran tamaño.
- Esta respuesta, conocida como "tetera", era demasiado grande para ser procesada por la aplicación, lo que provocaba que se bloqueara.
- La vulnerabilidad fue descubierta el 1 de diciembre de 2023 por el investigador de seguridad Kevin Beaumont.
- El encabezado específico que utilizaba el atacante era el encabezado "X-Uber-Client-Version".
- Uber estima que la vulnerabilidad podría haber afectado a hasta 10 millones de usuarios.

## Exchange ProxyNotShell

- Vulnerabilidad zero-day en Microsoft Exchange Server 2013, 2016 y 2019.
- Permite a los atacantes ejecutar código arbitrario en el servidor.
- Los atacantes pueden utilizar esta vulnerabilidad para robar datos, instalar malware o comprometer el servidor de forma permanente.
- CVE-2022-41040: Vulnerabilidad de falsificación de solicitud del lado del servidor (SSRF) que permite al atacante realizar solicitudes HTTP a cualquier dirección web.
- CVE-2022-41082: Vulnerabilidad de ejecución remota de código (RCE) que permite al atacante ejecutar código arbitrario en el servidor.

## The MOVEit Transfer vulnerability, CVE-2023-3436

- Es una vulnerabilidad de inyección SQL que afecta a la aplicación web MOVEit Transfer.
- La vulnerabilidad permite a un atacante no autenticado inyectar código SQL arbitrario en la db de MOVEit Transfer.
- La vulnerabilidad se encuentra en la función `executeQuery()` de la clase `QueryManager` de MOVEit Transfer.
- La vulnerabilidad se produce cuando la función executeQuery() recibe una consulta SQL que contiene una referencia circular a un objeto de flujo de objeto PDF.
- Actualizar a la versión 2023.0.2 (15.0.2) o posterior de MOVEit Transfer.
