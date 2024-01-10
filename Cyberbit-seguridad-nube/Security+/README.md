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

## Lesson 2B: Threat Intelligence

- **Fuentes de Investigación sobre Amenazas**
  + Foros de Hackers: Sitios web clandestinos donde los hackers comparten información sobre vulnerabilidades, exploits y herramientas. Ejemplo: "ExploitDB".
  + Blogs de Seguridad: Fuentes de noticias e investigación mantenidas por expertos en seguridad, informando sobre amenazas emergentes y análisis de ataques. Ejemplo: "Krebs on Security".
  + Informes de Amenazas: Documentos publicados por organizaciones de seguridad o investigadores individuales con detalles sobre campañas de amenazas específicas y recomendaciones de mitigación. Ejemplo: "Verizon Data Breach Investigations Report".
- **Deep Web**
  + Una parte oculta de Internet que no indexa por los buscadores habituales.
  + Contiene contenido legal e ilegal, como mercados negros y foros clandestinos.
  + Anonimato, alto riesgo de encontrar malware y contenido ilícito.
- **Proveedores de Inteligencia de Amenazas**
  + Datos de Comportamiento: Analizan patrones de actividad maliciosa para detectar amenazas. Ejemplo: ThreatQuotient, Palo Alto Networks.
  + Datos de Reputación: Asignan puntuaciones de riesgo a IPs, dominios y URLs. Ejemplo: PhishTank, Cisco Talos.
  + Datos de Amenazas: Proveen acceso a información sobre vulnerabilidades, exploits, campañas de malware y actores maliciosos. Ejemplo: Recorded Future, Mandiant.
  + SIEM (Sistemas de Gestión de Información y Eventos de Seguridad): Recolectan y analizan datos de seguridad de múltiples fuentes para identificar amenazas. Ejemplo: ArcSight, Splunk.
- **Modelos Comerciales de Inteligencia de Amenazas**
  + Freemium: Acceso básico gratuito con características limitadas, pago por funciones avanzadas.
  + Suscripción: Pago mensual o anual por acceso completo a los servicios.
  + Consultoría: Servicios profesionales de análisis de amenazas e implementación de soluciones.
- **IoC (Indicadores de Compromiso)**
  + Evidencias observables de una intrusión o actividad maliciosa.
  + IP maliciosa, URL con phishing, hash de malware, comportamiento de red sospechoso.
- **Fuentes de Datos de Amenazas**
  + Oasis: Estándar abierto para compartir IoC entre organizaciones.
  + STIX (Structured Threat Information eXchange): Lenguaje formal para representar información sobre amenazas.
  + TAXII (Threat Actor Exchange Indicator Information): Protocolo para el intercambio de IoC y STIX.
  + AIS (Automated Indicator Sharing): Sistema automatizado para compartir IoC en tiempo real.
- **Mapas de Amenazas**
  + Visualizaciones que representan el panorama de amenazas, mostrando actores, campañas, vectores de ataque y relaciones entre ellos.

<p align="center">
  <img src="https://www.silobreaker.com/wp-content/uploads/2023/06/Threat-Intel-Cycle-Wheel-Graphic-1024x629.png"/>
</p>

## Lesson 2B: Attack Frameworks and Indicator Management

- **Investigación de amenazas (Pirámide del Dolor CTI)**
  + La investigación de amenazas es el proceso de recopilar, analizar y compartir información sobre las amenazas cibernéticas.
  + El objetivo de la investigación de amenazas es mejorar la comprensión de las amenazas, lo que puede ayudar a las organizaciones a protegerse mejor contra ellas.
  + La pirámide del dolor CTI (Cyber Threat Intelligence) es un marco conceptual que ayuda a clasificar la información de inteligencia de amenazas según su valor y la dificultad para cambiarla por parte de los adversarios.
  + Esta pirámide tiene tres niveles: indicadores, tácticas, técnicas y procedimientos (TTPs), y contexto.
  + Los indicadores son datos específicos, como direcciones IP o hashes, que pueden cambiar fácilmente.
  + Las tácticas, técnicas y procedimientos son patrones de comportamiento de los atacantes
  + El contexto proporciona información sobre las motivaciones y objetivos de los adversarios.
<p align="center">
  <img src="https://media.licdn.com/dms/image/D4D12AQGd2YCEuIl21Q/article-inline_image-shrink_1500_2232/0/1674720822041?e=1709769600&v=beta&t=J2_QT7czQGiy22QBXS0LYKV-ddnpkBxIZxHcXS9Mu80"/>
</p>

- **Cyber Kill Chain**
  +  Es un modelo que describe las fases secuenciales que un adversario sigue para llevar a cabo un ataque.
  +  Reconnaissance: El atacante recopila información sobre el objetivo.
  + Intrusion: El atacante entra en el sistema del objetivo.
  + Exploitation: El atacante explota una vulnerabilidad para obtener acceso a los sistemas del objetivo.
  + Installation: El atacante instala malware o software malicioso en los sistemas del objetivo.
  + Command and Control: El atacante controla el malware o el software malicioso a través de un servidor de comando y control.
  + Actions on Objectives: El atacante realiza acciones en los sistemas del objetivo, como robar datos o interrumpir las operaciones.
  +  Comprender estas etapas ayuda a las organizaciones a desarrollar estrategias para prevenir, detectar y responder a los ataques en cada fase.
<p align="center">
  <img src="https://seqred.pl/wp-content/uploads/2020/08/cyber-kill-chain-process.png"/>
</p>  

- **MITRE ATT&CK**
  + MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) es un marco de trabajo que describe las TTP utilizados por los atacantes en cada fase del ciclo de vida del ataque.
  + Organizado en matrices, proporciona un panorama completo de las acciones que los adversarios pueden llevar a cabo.
  + Permite a los profesionales de seguridad comprender y mejorar sus defensas.
  + El marco se divide en 14 grupos de tácticas y más de 300 técnicas.
- **Diamond Model of Intrusion Analysis**
  + Este modelo se basa en cuatro componentes: adversario, infraestructura, capacidad y víctima.
  + Ayuda a los analistas a entender las relaciones entre estos elementos y a analizar intrusiones desde una perspectiva más holística.
  + La idea central es ver cómo un adversario selecciona sus objetivos, utiliza ciertas capacidades y aprovecha la infraestructura para afectar a una víctima.
  + Context: El contexto del ataque, que incluye la información sobre el objetivo, el atacante y el entorno.
  + Indicators: Los indicadores de ataque, que son las evidencias de un ataque.
  + Observables: Los observables, que son los datos que se pueden recopilar de un sistema o red.
  + Hypotheses: Las hipótesis, que son las posibles explicaciones de un ataque.
<p align="center">
  <img src="https://uploads-us-west-2.insided.com/cymulate-en/attachment/4d11266f-8ee0-4855-aabb-9b40f89e73d9.png"/>
</p>  
    
- **STIX, TAXII, OpenIOC, MISP**
  + Son formatos de intercambio de información de inteligencia de amenazas.
  + Estos formatos se utilizan para compartir información de inteligencia de amenazas entre diferentes organizaciones.
  + STIX: es un formato estándar para representar información de inteligencia de amenazas.
  + TAXII: es un protocolo de transferencia de datos para STIX.
  + OpenIOC: es un formato abierto para representar información de inteligencia de amenazas.
  + MISP: es un sistema de gestión de información de seguridad (SIEM) que admite STIX, TAXII y OpenIOC.
    
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

-
-


