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
- 
## Introduction to Windows Credentials and Credentials Dumping

## Introduction to Mimikatz

## Malicious use of Registry
