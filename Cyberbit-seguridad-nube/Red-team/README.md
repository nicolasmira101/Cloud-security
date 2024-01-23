# Red Team

## Brute Ratel C4

- Es una herramienta de post-explotación gratuita y de código abierto desarrollada por Chatan Nayak.
- Ejecución de comandos: Permite ejecutar comandos en el sistema comprometido.
- Intercepción de tráfico: Permite interceptar el tráfico de red entre el sistema comprometido y el atacante.
- Evasión de detección: Incluye una serie de técnicas para evitar la detección por parte de las soluciones de seguridad.
- Automatización de tareas: Permite automatizar tareas de post-explotación mediante scripts.
- está escrita en Python y se ejecuta como un agente en el sistema comprometido. La herramienta se comunica con el atacante a través de un canal de comunicación cifrado.

<p align="center">
  <img src="https://imgur.com/mhUBVoW.png"/>
</p>

## Sliver Framework

- Es un framework de código abierto (open-source) y multiplataforma para la emulación de adversarios y la simulación de amenazas.
- Su objetivo principal es proporcionar a los equipos de seguridad una herramienta para simular ataques avanzados y evaluar las capacidades de defensa de sus sistemas.
- Permite a los "red teams" controlar de forma remota dispositivos infectados (implantes) y ejecutar diversas acciones maliciosas para imitar las técnicas de los atacantes reales.
- Comunicación C2 flexible: Soporta comunicación cifrada a través de distintos protocolos
- Generación dinámica de código: Compila los implantes con claves de cifrado asimétricas únicas para dificultar su detección y análisis.
- Ofuscación en tiempo de compilación: Dificulta aún más el análisis de los implantes por parte de los defensores.
- Multiplataforma: Compatible con Windows, macOS y Linux, tanto para el servidor de control como para los implantes.
- Soporte multiusuario: Permite la colaboración entre múltiples miembros del equipo de seguridad.
- Ejecución de código arbitrario
- Exfiltración de datos
- Persistencia
- Evasión de defensas
- Movimiento lateral
- Posibilidad de scripting con JavaScript/TypeScript o Python
- Escrito en Golang, un lenguaje de programación conocido por su rendimiento y seguridad.
- Su código fuente está disponible en GitHub, lo que permite a los expertos en seguridad analizarlo y contribuir a su desarrollo.
- Se ha convertido en una herramienta popular entre los "red teams" debido a su flexibilidad, facilidad de uso y potentes funcionalidades.
 
## Shikata-Ga-Nai

- Shikata-Ga-Nai, significa "no se puede evitar" en japonés.
- Cifra payloads de malware para dificultar su detección por las herramientas de seguridad.
- Utiliza instrucciones FPU antiguas para calcular la dirección de la siguiente instrucción a descifrar.
- Utiliza un esquema de cifrado XOR avanzado.
- El esquema de descifrado utiliza una clave secreta y un contador para descifrar cada byte del payload.
- Se ha utilizado en una variedad de tipos de malware, incluidos ransomware, trojanos y malware de robo de información.
 
## Alchimist Framework

- Alchimist es un framework de ataque de origen chino que se compone de un backend C2 y un troyano de acceso remoto (RAT).
- Está diseñado para permitir controlar y recopilar datos de dispositivos comprometidos.
- Está escrito en Go y se ejecuta en un servidor web.
- La RAT, llamada Insekt, también está escrita en GoLang y es multiplataforma.
- Insekt proporciona a los atacantes una variedad de capacidades, incluyendo la recopilación de información, la toma de capturas de pantalla, la ejecución de comandos, la ejecución de shellcode, el escaneo de redes y la manipulación de SSH.
- Utiliza un modelo de cliente-servidor, con un servidor central que se comunica con agentes instalados en dispositivos comprometidos.
- Puede controlar y recopilar datos de una variedad de dispositivos, incluidos sistemas operativos Windows, macOS y Linux, así como dispositivos móviles.
- Mantener los sistemas actualizados con las últimas correcciones de seguridad.
- Usar firewalls y sistemas de detección de intrusiones (IDS).
- Educar a los empleados sobre la seguridad cibernética.
- Utilizar soluciones de seguridad que bloqueen Alchimist y Insekt.
- Monitorear el tráfico de red para detectar actividad sospechosa.
- Implementar un proceso de respuesta a incidentes de seguridad.

## Introduction to Privilege Escalation

- Permite al atacante obtener un control total sobre el sistema o red objetivo.
- El atacante busca explotar vulnerabilidades en el sistema operativo, las aplicaciones o la configuración de seguridad para obtener privilegios elevados.
- Escalada vertical: se produce cuando un atacante obtiene privilegios de mayor nivel que los que tenía inicialmente. Por ejemplo, un usuario normal puede obtener privilegios de administrador.
- Escalada horizontal: se produce cuando un atacante obtiene acceso a recursos o sistemas que no le estaban permitidos. Por ejemplo, un usuario de una aplicación puede obtener acceso a los datos de otro usuario.
- **Herramientas**
  + Metasploit: Es un framework de hacking ético que incluye una amplia gama de módulos para escalar privilegios.
  + PowerUpKit: Es una colección de herramientas y scripts diseñados para escalar privilegios en sistemas Windows.
  + LinEnum: Es una herramienta de línea de comandos para enumerar los privilegios de un usuario en sistemas Linux.
- **Técnicas**
  + Explotación de vulnerabilidades: Los atacantes pueden buscar vulnerabilidades en el sistema operativo, las aplicaciones o la configuración de seguridad para explotarlas y obtener privilegios elevados.
  + Utilización de exploits conocidos: Los atacantes pueden utilizar exploits conocidos que se han publicado en línea.
  + Desarrollo de exploits personalizados: Los atacantes pueden desarrollar exploits personalizados para vulnerabilidades específicas.
  + Uso de herramientas de línea de comandos: Los atacantes pueden utilizar herramientas de línea de comandos para aprovechar     	  vulnerabilidades o realizar cambios en la configuración del sistema.
- Ejemplo LinEnum
```
# LinEnum

# Escaneando el sistema...

[+] Sistema operativo: Ubuntu 22.04
[+] Usuario actual: user
[+] Grupo actual: users

# Privilegios del usuario actual

[+] Sudo: habilitado
[+] Sudoers: user ALL=(ALL) NOPASSWD: ALL

# Escalando privilegios...

# Ejecutando el comando sudo con la opción -i

sudo -i

# Cambiando al usuario root

whoami
root
```

- Ejemplo PowerUpKit
```
# PowerUpKit

# Escaneando el sistema...

[+] Sistema operativo: Windows 10
[+] Usuario actual: user
[+] Grupo actual: Users

# Privilegios del usuario actual

[+] Sesión: interactiva
[+] Control total del equipo: no
[+] Sesión con privilegios elevados: no

# Escalando privilegios...

# Ejecutando el exploit ms16-075

PowerUpKit.ps1 -Exploit ms16-075

# Cambiando al usuario administrador

whoami
administrator
```  
## Introduction to Windows Credentials and Credentials Dumping

- El Local Security Authority Subsystem Service (LSASS) es un servicio de Windows que proporciona funciones de seguridad, como la autenticación de usuarios y la gestión de contraseñas.
- El LSASS almacena las credenciales de los usuarios en un archivo llamado `ntdll.dll`.
- Las contraseñas de los usuarios se almacenan en el registro de Windows en forma de hash.
- Las credenciales de los usuarios, como las contraseñas de las redes Wi-Fi y las cuentas de servicio web, se almacenan en el archivo `Credential Manager`.
- Las credenciales de los usuarios se almacenan en la memoria cuando un usuario está autenticado.
- En un entorno de dominio, los usuarios se autentican con el servidor de dominio.
- El servidor de dominio almacena las contraseñas de los usuarios en Active Directory.
- Lightweight Directory Access Protocol (LDAP) es un protocolo de acceso a directorios que se utiliza para acceder a Active Directory.
- LDAP se puede utilizar para recuperar las credenciales de los usuarios desde Active Directory.
- Credentials dumping es el proceso de recuperar las credenciales de un usuario.
- Los atacantes pueden utilizar el credentials dumping para obtener acceso a los sistemas y redes de una organización.
- Proteger las credenciales
  + Utilizar contraseñas seguras
  + Habilitar la autenticación multifactor (MFA)
  + Actualizar los sistemas operativos y las aplicaciones
  + Los usuarios deben ser educados sobre las mejores prácticas de seguridad de contraseñas.
    
## Introduction to Mimikatz

## Malicious use of Registry
