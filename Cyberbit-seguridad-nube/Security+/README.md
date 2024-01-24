# Security+

## Lesson 15A: Secure Cloud & Virtualization Services

- Los servicios de nube y virtualización ofrecen muchas ventajas, pero también presentan riesgos de seguridad.
- Los profesionales de seguridad deben comprender estos riesgos y cómo mitigarlos.
- **Riesgos de seguridad en la nube**
  + La nube introduce nuevos desafíos en la autenticación y autorización.
  + Los administradores de la nube deben implementar controles de acceso efectivos para proteger los recursos de la nube.
  + Los datos almacenados en la nube deben estar protegidos contra el acceso no autorizado, la modificación y la destrucción.
  + La red de la nube debe estar protegida contra ataques externos e internos.
  + Los hosts de la nube deben estar protegidos contra malware y otras amenazas.
  + Las aplicaciones de la nube deben estar protegidas contra vulnerabilidades y ataques.
- **Mitigando los riesgos de seguridad en la nube**
  + El modelo de seguridad de confianza cero asume que ningún usuario o dispositivo es de confianza de forma predeterminada.
  + Los controles de seguridad de la nube deben implementarse para proteger los recursos de la nube contra los riesgos identificados.
  + Los usuarios de la nube deben ser educados sobre las mejores prácticas de seguridad.
- La creación y proliferación incontroladas de máquinas virtuales (VM) pueden provocar ineficiencias, vulnerabilidades de seguridad y aumento de los costes.
- La falta de políticas, las máquinas virtuales redundantes, la sobreestimación de las necesidades de recursos y las operaciones de TI aisladas contribuyen al crecimiento incontrolado.
- Despilfarra recursos, complica la gestión, aumenta los riesgos de seguridad y dificulta la optimización de los recursos.
- Políticas de provisión de máquinas virtuales
- Directrices de asignación de recursos
- Gestión del ciclo de vida de las máquinas virtuales
- Asegúrate de que las máquinas virtuales se asignan recursos apropiados para sus cargas de trabajo, evitando la sobreprovisionación.
- Reduce el número de máquinas virtuales que hay que gestionar y parchear, reduciendo las vulnerabilidades de seguridad.
- Implementa controles de acceso granulares para limitar el acceso a las máquinas virtuales y sus datos.
- Realiza auditorías de seguridad de las máquinas virtuales y el entorno virtual para identificar posibles vulnerabilidades.
- El escape de VM es un tipo de ataque cibernético que permite a un atacante tomar el control de una máquina virtual (VM) que se ejecuta en un entorno virtualizado.

## Security+ Lesson 15B: Cloud Security Solutions

- **Integración y Auditoría de la Seguridad en la Nube**
  + Identidad y acceso: Asegurar que solo los usuarios autorizados tengan acceso a los recursos de la nube.
  + Seguridad de la red: Proteger el tráfico de red entre la nube y tu infraestructura local.
  + Seguridad del almacenamiento: Proteger los datos almacenados en la nube.
  + La auditoría de la configuración y actividad de la nube es esencial para identificar y corregir las vulnerabilidades de seguridad.
- **Controles de Seguridad en la Nube**
  + Los controles de seguridad en la nube son las medidas que se implementan para proteger los recursos de la nube.
  + Preventivos: Disuaden o evitan que se produzcan ataques. Por ejemplo, el cifrado de datos.
  + Detectivos: Detectan los ataques que han tenido éxito. Por ejemplo, el monitoreo de eventos de seguridad.
  + Correctivos: Recuperan los sistemas afectados por un ataque. Por ejemplo, la restauración de copias de seguridad.
- **Seguridad de la Computación en la Nube**
  + Las instancias de máquinas virtuales (VM) y los contenedores son los recursos de computación más comunes en la nube.
  + Seguridad de la imagen: Asegurar que la imagen de la VM o el contenedor esté libre de vulnerabilidades.
  + Seguridad de la configuración: Asegurar que la configuración de la VM o el contenedor sea segura.
  + Seguridad de los usuarios y permisos: Asegurar que solo los usuarios autorizados tengan acceso a la VM o el contenedor.
- **Seguridad del Almacenamiento en la Nube**
  + Los datos almacenados en la nube son un objetivo atractivo para los atacantes.
  + Cifrado: Cifrar todos los datos almacenados en la nube.
  + Control de acceso: Asegurar que solo los usuarios autorizados tengan acceso a los datos.
  + Auditoría de registros: Auditar los registros de acceso a los datos para detectar actividad sospechosa.
- **Alta Disponibilidad**
  + Es la capacidad de un sistema para continuar funcionando incluso en caso de fallas.
  + Redundancia: Tener recursos redundantes para que puedan asumir el control en caso de falla.
  + Recuperación ante desastres: Tener un plan de recuperación ante desastres para restaurar los sistemas en caso de una falla catastrófica.
  + Balanceo de carga: Distribuir el tráfico entre varios recursos para mejorar el rendimiento y la disponibilidad.
- **Seguridad de la Red en la Nube**
  + La red es la infraestructura que conecta los recursos de la nube entre sí y con el mundo exterior.
  + Firewalls: Filtrar el tráfico de red para bloquear el tráfico no autorizado.
  + VPN: Proporcionar acceso seguro a la red desde dispositivos remotos.
  + Análisis de tráfico de red: Monitorear el tráfico de red para detectar actividad sospechosa.
- **Puntos Finales VPC**
  + Son recursos de red que permiten conectar de forma segura recursos dentro de una VPC con servicios de AWS sin necesidad de un internet gateway público.
  + Los puntos finales VPC pueden ayudar a mejorar la seguridad y el control del tráfico de red.
- **Seguridad de Firewalls en la Nube**
  + Los firewalls son dispositivos de seguridad que filtran el tráfico de red.
  + Los firewalls en la nube pueden ayudar a proteger los recursos de la nube de ataques entrantes.
- **Grupos de Seguridad**
  + Son reglas que controlan el acceso a las instancias de una VPC.
  + Los grupos de seguridad pueden ayudar a aumentar la seguridad granular de la red cloud.
- **Agente de Seguridad de Acceso a la Nube (CASB)**
  + Los CASB son soluciones de seguridad que ayudan a controlar el uso de aplicaciones en la nube por parte de los usuarios.
  + Los CASB pueden ayudar a prevenir la fuga de datos y proteger contra amenazas cloud-based.
    
## Lesson 2A: Threat Actors & Attack Surface

- **Vulnerabilidad, Amenaza, Riesgo y Control**
  + Vulnerabilidad: Un defecto o debilidad en un sistema, red o aplicación que puede ser explotada por un atacante.
  + Amenaza: Un actor, evento o circunstancia con el potencial de causar daño a un activo.
  + Riesgo: La probabilidad de que una amenaza se materialice y cause un daño.
  + Control: Una medida o acción que se implementa para mitigar el riesgo.
- **Atributos de los Actores de la Amenaza**
  + Intención: El propósito del atacante. Puede ser por diversión, robo, sabotaje, etc.
  + Motivación: La razón por la que el atacante quiere lograr su intención. Puede ser ideológica, financiera o personal.
  + Sofisticación: El nivel de conocimiento y experiencia del atacante. Puede ir desde script kiddies hasta hackers expertos.
  + Capacidad: Los recursos técnicos y humanos del atacante.
  + Financiación: El dinero o los recursos que el atacante tiene a su disposición.
- **Tipos de Hackers**
  + Los hackers se pueden clasificar en diferentes tipos según su intención, motivación y sofisticación.
  + Script kiddies: Hackers novatos que usan herramientas automatizadas para realizar ataques simples.
  + Hacktivistas: Hackers con motivaciones ideológicas que utilizan sus habilidades para protestar o causar daños.
  + Cibercriminales: Hackers que realizan ataques con fines lucrativos, como robar datos o dinero.
  + Actores estatales: Hackers patrocinados por gobiernos que llevan a cabo ataques para recopilar inteligencia o realizar operaciones de espionaje.
  + APT: Amenazas Persistentes Avanzadas son ataques dirigidos por actores estatales que suelen estar dirigidos a objetivos específicos, como sistemas gubernamentales o empresas críticas.
- **Actores de Amenaza Interna**
  + Son empleados o individuos con acceso privilegiado a un sistema o red que podrían abusar de su posición para realizar ataques.
  + Estos ataques pueden ser tan o más peligrosos que los ataques externos, ya que el atacante tiene un conocimiento íntimo del sistema o red.
- **Superficie de Ataque**
  + Es el conjunto de todos los puntos de entrada potenciales a un sistema o red.
  + Cuanto mayor sea la superficie de ataque, más vulnerable será el sistema o red.
  + Sistemas: Servidores, ordenadores, dispositivos móviles, etc.
  + Puertos: Puertos de red abiertos que pueden ser utilizados por atacantes.
  + Aplicaciones: Aplicaciones web, aplicaciones móviles, etc.
  + Dispositivos: Dispositivos conectados a la red, como impresoras, cámaras, etc.
- **Vectores de Ataque**
  + Son los medios que utilizan los atacantes para acceder a un sistema o red.
  + Phishing: Envío de mensajes de correo electrónico fraudulentos que intentan engañar a los usuarios para que revelen información confidencial.
  + Vulnerabilidades de software: Debilidades en el software que pueden ser explotadas por atacantes.
  + Ataques de fuerza bruta: Intentos repetidos de adivinar una contraseña o clave.
  + Inyección de código: Inserción de código malicioso en un sistema o red.

<p align="center">
  <img src="https://www.cloudflare.com/resources/images/slt3lc6tev37/oUd084IG6Zq2dW6mI1TT7/891a2c62bec90326d560326e8790a5ed/what_is_an_attack_vector.png"/>
</p>
    
## Lesson 18A: Digital Forensics Documentation

- **Informática Forense**
  + Proceso de recopilación, análisis y preservación de evidencia electrónica para investigar y prevenir ciberdelitos.
  + Involucra la examinación de dispositivos digitales, redes y datos para descubrir rastros de actividades maliciosas.
- **Evidencia**
  + La evidencia digital incluye archivos, registros, correos electrónicos y otros artefactos electrónicos.
  + La evidencia admisible debe ser relevante, auténtica y obtenida legalmente.
- **Documentación y Admisibilidad**
  + Una documentación adecuada es crucial para mantener la integridad de la investigación.
  + La admisibilidad depende de cumplir con estándares legales y garantizar la Cadena de Custodia.
- **Debido proceso**
  + Adherencia a procedimientos legales y respeto de los derechos individuales durante investigaciones digitales.
  + Asegura la credibilidad y legitimidad del proceso forense.
- **Orden Legal de Conservación (Legal Hold)**
  + Proceso de preservar y proteger evidencia potencial de alteraciones o eliminación.
  + Implementado para cumplir con requisitos legales y prevenir la destrucción intencional.
- **Cadana de custodio**
  + Un rastro documentado que registra la manipulación y transferencia de evidencia desde su recolección hasta su presentación en la corte.
  + Esencial para establecer la confiabilidad de la evidencia en procedimientos legales.
- **Informes de Informática Forense**
  + Documentación integral que resume toda la investigación forense digital.
  + Incluye hallazgos, análisis, metodologías, herramientas utilizadas y conclusiones.
  + Los informes deben ser claros, concisos y adecuados para audiencias técnicas y no técnicas. 
- **E-Discovery**
  + Proceso de identificación, recopilación y preservación de información almacenada electrónicamente (ESI) para casos legales.
  + Involucra el uso de herramientas especializadas para buscar, filtrar y presentar evidencia digital relevante.
- **Entrevistas a Testigos y Grabaciones de Video**
  + Realización de entrevistas con personas involucradas o relevantes para la investigación.
  + Las entrevistas en video ayudan a capturar señales no verbales, mientras que las notas detalladas documentan información verbal.
  + Asegura una comprensión integral del incidente y ayuda a corroborar evidencia digital.
- **Líneas de tiempo**
  + Representación gráfica de eventos que ayuda a los investigadores entender el orden cronológico de los incidentes.
  + Facilita la identificación de patrones y relaciones.
  + Ajuste por diferencias de tiempo entre sistemas para sincronizar las líneas de tiempo de eventos de manera precisa.
  + Fundamental para la reconstrucción de la secuencia de eventos durante un incidente.
  + Reconocimiento de la posibilidad de manipulación de relojes o marcas de tiempo del sistema.
  + Implementación de medidas para detectar y mitigar riesgos de manipulación.
- **Logs y tráfico de red**
  + Análisis de registros de sistema y tráfico de red en busca de rastros de acceso no autorizado o actividades maliciosas.
  + Los logs proporcionan un registro cronológico de eventos, facilitando la reconstrucción de incidentes.
- **Inteligencia Estratégica y Contrainteligencia**
  + Utilización de la recopilación de inteligencia para defender proactivamente contra amenazas cibernéticas.
  + La contrainteligencia implica identificar y mitigar riesgos planteados por actores maliciosos.
  + La inteligencia estratégica guía la toma de decisiones para mejorar la postura general de ciberseguridad.
    
## Lesson 18B: Digital Forensics Evidence Acquisition

- **Orden de volatilidad**
  + La evidencia digital se deteriora a diferentes velocidades según su volatilidad.
  + Los datos más volátiles desaparecen con el apagado de la alimentación (registradores, caché de memoria).
  + Los datos menos volátiles persisten entre reinicios (datos de disco).
  + La adquisición sigue este orden, dando prioridad a las fuentes más volátiles primero.
- **Proceso de adquisición**
  + Planificación: Identificar las fuentes de evidencia, comprender los requisitos legales, documentar los procedimientos.
  + Preparación: Asegurar la escena, aislar los dispositivos, documentar el entorno.
  + Adquisición: Recopilar evidencia utilizando las herramientas y técnicas adecuadas.
  + Verificación: Garantizar la integridad y autenticidad de los datos.
  + Documentación: Registrar las actividades y mantener la cadena de custodia.
- **Software de forense digital**
  + Encase: Herramienta comercial potente para el análisis forense de discos, la creación de imágenes forenses y la recuperación de datos.
  + Autopsy: Plataforma de código abierto para el análisis de imágenes, la forense de memoria y la investigación de malware.
  + WinHex: Editor de discos versátil para la inspección de datos en hexadecimal, la recuperación de evidencia y el tallado de archivos.
  + Volatility Framework: Herramienta de forense de memoria para analizar imágenes de memoria en vivo y adquiridas, investigar módulos del kernel e identificar artefactos de malware.
- **Adquisición de memoria del sistema**
  + Memoria del sistema: Elemento más volátil, que contiene procesos activos, módulos cargados y datos temporales.
  + Adquisición en vivo: Captura el estado de la memoria mientras el sistema está en funcionamiento, utilizando herramientas de hardware o software dedicadas.
  + Volcado de bloqueo: Se escribe automáticamente en el disco cuando el sistema se bloquea, proporcionando datos forenses valiosos.
  + Archivo de hibernación: Contiene el estado del sistema guardado para reanudar el trabajo más tarde, ofreciendo información sobre la actividad reciente.
  + Archivo de paginación: Utilizado por Windows para extender la memoria RAM física con espacio en disco, potencialmente conteniendo evidencia valiosa.
- **Adquisición de imágenes de disco**
  + Imagen de disco: Copia exacta de los sectores del disco, conservando todos los datos, incluidos los archivos eliminados y el espacio libre.
  + Adquisición en vivo: Captura la imagen mientras el sistema está en funcionamiento, conservando datos volátiles como archivos abiertos y entradas del registro.
  + Adquisición estática: Adquiere la imagen después del apagado del sistema, ideal para mantener la integridad de los datos pero que falta evidencia volátil.
  + Herramientas: Encase, FTK Imager, Autopsy Imager, dd (línea de comandos de Linux)
- **Preservación e integridad de la evidencia**
  + Procedencia: Documentación de la cadena de custodia, que registra cada paso desde la recopilación de evidencia hasta el análisis.
  + Adquisición de datos: Utilizar técnicas que no alteren los datos originales, como bloqueadores de escritura y herramientas de creación de imágenes forenses.
  + Preservación de la evidencia: Almacenar la evidencia de forma segura, mantener la cadena de custodia y evitar la contaminación.
- **Adquisiciones de otros datos**
  + Tráfico de red: Capturar paquetes de red utilizando taps de red o dispositivos de análisis forense para investigar incidentes basados ​​en la red.
  + Caché: Almacenamiento temporal para contenido web, historial del navegador y datos de aplicaciones. La adquisición puede revelar la actividad del usuario y la evidencia oculta.
  + Artefactos: Archivos o entradas del registro creados por malware o actividad específicos, utilizados para su identificación e investigación.
  + Recuperación de datos: Técnicas para recuperar archivos eliminados o dañados de dispositivos de almacenamiento. Útil para reconstruir eventos y encontrar evidencia oculta.
  + Instantánea: Copia estática del estado de una máquina virtual en un punto específico en el tiempo, que ofrece oportunidades de análisis forense.
  + Firmware: Código de bajo nivel en dispositivos de hardware.
- **Análisis forense digital para la nube**
  + SLA (Acuerdo de nivel de servicio): Define las políticas de retención de datos y los procedimientos de acceso para los proveedores de la nube.
  + Imágenes efímeras: Instancias de máquinas virtuales de corta duración en un entorno de nube, que requieren técnicas especiales para su adquisición y análisis.
  + Problemas de cadena de custodia: Complejidades debidas al almacenamiento remoto y a la infraestructura distribuida de la nube.
  + Problemas de jurisdicción: La ubicación de los datos puede no coincidir con la autoridad legal del investigador, lo que requiere cooperación internacional.
  + Leyes sobre violación de datos: Normativas como GDPR e HIPAA imponen responsabilidades en materia de seguridad de datos y notificación de violaciones.


