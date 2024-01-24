# Inteligencia de amenazas

## MISP

- MISP (Malware Information Sharing Platform & Threat Sharing) es una plataforma de código abierto diseñada para facilitar el intercambio de información sobre amenazas entre organizaciones.
- Su principal objetivo es mejorar la capacidad de detección y respuesta ante amenazas.
- Permite que las organizaciones compartan de manera segura información sobre indicadores de compromiso (IoCs) y tácticas, técnicas y procedimientos (TTPs).
- Utiliza formatos de intercambio de información estandarizados, como STIX y TAXI, para asegurar la interoperabilidad y la consistencia en la representación de la información de amenazas.
- Promueve la colaboración en comunidades más amplias, como sectores industriales o regiones geográficas.
- Permite correlacionar y relacionar diferentes tipos de datos de amenazas, proporcionando una visión más completa de las amenazas.
- Permite a las organizaciones almacenar, gestionar y compartir indicadores de compromiso, como direcciones IP maliciosas, hashes de archivos, URLs sospechosas, etc.
- Facilita el análisis de amenazas mediante la agregación y correlación de datos provenientes de diversas fuentes.
- Ofrece notificaciones automáticas sobre cambios en la información compartida.
- Las organizaciones pueden crear y editar eventos de amenazas, que incluyen información sobre IOC, actores de amenazas y vulnerabilidades.

<p align="center">
  <img src="https://www.misp-project.org/img/carousel/visualization.png"/>
</p>
 
## Threat Intelligence Circle Phase 1 - Planning

- Es el primer paso para establecer un programa de inteligencia de amenazas eficaz.
- Identificación de los objetivos y metas específicas de la inteligencia de amenazas.
- Determinación de las áreas críticas y activos a proteger.
- Mejorar la visibilidad de las amenazas.
- Reducir el riesgo de ataques.
- Mejorar la toma de decisiones de seguridad.
- Establecimiento del alcance de la inteligencia de amenazas, incluyendo las áreas geográficas y los tipos de amenazas a investigar.
- Reconocimiento de las limitaciones y restricciones, como recursos disponibles y restricciones legales.
- Identificación de fuentes de información relevantes, como fuentes abiertas, feeds de amenazas, informes gubernamentales y colaboración con la comunidad de seguridad.
- Formación de un equipo dedicado a la inteligencia de amenazas con roles y responsabilidades claramente definidos.
- Establecimiento de procedimientos para la gestión de la información y la toma de decisiones.
- El análisis de riesgos debe identificar las amenazas que son más relevantes para la organización.
- El plan de recopilación de inteligencia debe definir las fuentes de inteligencia que se utilizarán.
- El plan de análisis de inteligencia debe definir los métodos que se utilizarán para analizar la inteligencia
- Revisión de las consideraciones legales y éticas asociadas con la recopilación, análisis y distribución de inteligencia de amenazas.
- Garantía de conformidad con las leyes y regulaciones locales e internacionales.
- Identificación y evaluación de posibles riesgos asociados con la implementación de la inteligencia de amenazas.
- Desarrollo de estrategias para mitigar y gestionar estos riesgos.
- Desarrollo e implementación de la infraestructura tecnológica necesaria para la recopilación y análisis de datos de amenazas.
- Garantía de la seguridad y confidencialidad de la información.
- Establecimiento de canales de comunicación efectivos tanto internos como externos.
- Fomento de la colaboración con otras organizaciones y la comunidad de seguridad.
  
## Threat Intelligence Circle Phase 2 – IoC Types and Tools

- Se centra en los Indicadores de Compromiso (IoC) y las herramientas asociadas. 
- Los Indicadores de Compromiso son evidencias de actividad maliciosa en sistemas informáticos.
- Esta fase implica la identificación y comprensión de diferentes tipos de IoC.
- IoC Básicos: incluyen direcciones IP, hashes de archivos y nombres de dominio que son fácilmente identificables.
- IoC Avanzados: involucran patrones de comportamiento, tácticas, técnicas y procedimientos (TTP), y firmas de malware más complejas.
- Plataformas de Inteligencia de Amenazas (TIP): Facilitan la recopilación, análisis y distribución de información de amenazas.
- Sistemas de Gestión de Eventos de Seguridad (SIEM): Ayudan a correlacionar eventos de seguridad y generan alertas basadas en IoC.

## Threat Intelligence Circle Phase 3-4 - Processing and Analysis

- Se centra en el procesamiento y análisis de la información de inteligencia de amenazas.
- Esta fase tiene como objetivo transformar los datos brutos en información procesable que se puede utilizar para tomar decisiones de seguridad. 
- **Proceso de Análisis de IoC**
  + Recopilación: Adquisición de IoC a través de diversas fuentes como feeds de inteligencia, análisis de incidentes y registros de eventos.
  + Normalización: Estandarización de los datos para facilitar el análisis y comparación.
  + Enriquecimiento: Agregación de información adicional para mejorar la comprensión del contexto.
  + Correlación: Relacionar IoC para identificar patrones y conexiones.
  + Análisis: Evaluación de la gravedad y relevancia de los IoC para la seguridad.
- **Análisis de Inteligencia de Amenazas**
  + Correlación de Datos: Se busca identificar patrones y relaciones entre diferentes conjuntos de datos para obtener una comprensión más profunda de las amenazas.
  + Análisis de TTP: Se examinan las tácticas utilizadas por los actores maliciosos, sus técnicas y procedimientos, con el objetivo de anticipar y prevenir futuros ataques.
  + Contextualización de amenazas: La información se contextualiza para comprender el alcance y la gravedad de las amenazas. Se evalúa la relevancia para la organización y se priorizan las acciones.
  + Generación de informes de inteligencia: La inteligencia obtenida se documenta en informes detallados que son comprensibles para los tomadores de decisiones. Estos informes incluyen recomendaciones y acciones mitigadoras.
  + Integración con sistemas de seguridad: La inteligencia de amenazas se integra con sistemas de seguridad, como firewalls y sistemas de detección de intrusiones, para fortalecer las defensas y la capacidad de respuesta.
  + Compartir inteligencia: Se destaca la importancia de compartir información de amenazas con otras organizaciones para mejorar la seguridad a nivel global.

## Threat Intelligence Circle Phase 5 - Dissemination and Feedback

- Aborda la distribución de la inteligencia generada y la retroalimentación recibida.
- **Distribución**
  + Identificación de audiencia objetivo: Se determina quiénes serán los receptores clave de la inteligencia generada, incluyendo equipos de seguridad, líderes de la organización y otros stakeholders relevantes.
  + Formatos de distribución: La inteligencia se distribuye de manera adaptada a diferentes formatos, como informes escritos, alertas automatizadas, actualizaciones de seguridad y sesiones de capacitación, según las necesidades de la audiencia.
  + Canales de distribución: Se utilizan canales seguros y eficientes para compartir la información de amenazas, como plataformas de inteligencia de amenazas, correos electrónicos seguros y sistemas internos de comunicación.
  + Accesibilidad y comprensión: Se asegura que la información sea fácilmente accesible y comprensible para la audiencia, con el objetivo de facilitar la toma de decisiones informada.
- **Feedback y Mejora Continua**
  +   Recolección de retroalimentación: Se busca activamente la retroalimentación de los receptores para evaluar la utilidad y la efectividad de la inteligencia proporcionada.
  + Evaluación de efectividad: Se analiza la forma en que la inteligencia de amenazas ha contribuido a la mejora de la postura de seguridad de la organización y a la mitigación de posibles amenazas.
  + Ajustes y mejoras: Basándose en la retroalimentación recibida, se realizan ajustes en los procesos, en la calidad de la inteligencia y en los métodos de distribución para mejorar continuamente el programa de inteligencia de amenazas.
  + Iteración del ciclo de inteligencia de amenazas: La retroalimentación informa la iteración continua del ciclo de inteligencia de amenazas, garantizando que el proceso evolucione para abordar las amenazas emergentes y las cambiantes necesidades de seguridad.
  + Comunicación de Éxitos y Desafíos: Se comunica de manera transparente sobre los éxitos logrados y los desafíos encontrados en el manejo de amenazas. Esto facilita la colaboración y el aprendizaje compartido tanto dentro de la organización como en la comunidad de seguridad.
