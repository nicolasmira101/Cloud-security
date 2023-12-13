# Microsoft Azure

## Características

- **Escalabilidad**: Permite aumentar o disminuir los recursos informáticos según las necesidades.
- **Flexibilidad**: Ofrece una amplia gama de servicios y herramientas para desarrolladores.
- **Pague por Uso**: Modelo de pago por consumo, lo que significa que solo se paga por los recursos que se utilizan.
- **Seguridad**: Ofrece protocolos y herramientas avanzadas de seguridad para proteger los datos y la infraestructura.
- **Alta Disponibilidad**: Garantiza la disponibilidad de aplicaciones y datos con un SLA (Acuerdo de Nivel de Servicio) confiable.

## Servicios

- **Cómputo**: Ofrece servicios como Máquinas Virtuales (VMs), Azure Kubernetes Service (AKS), Azure Functions (computación sin servidor), entre otros.
- **Almacenamiento**: Azure Storage proporciona almacenamiento en la nube para datos estructurados y no estructurados.
- **Redes**: Incluye servicios como Azure Virtual Network para conectar redes locales con la nube y Azure CDN para entrega de contenido.
- **Bases de Datos**: Ofrece bases de datos relacionales (Azure SQL Database) y no relacionales (Azure Cosmos DB).
- **Inteligencia Artificial y Análisis**: Azure Machine Learning, Azure Cognitive Services y Azure Synapse Analytics son algunos de sus servicios en este ámbito.
- **IoT**: Azure IoT Hub facilita la conexión, supervisión y gestión de dispositivos IoT.
- **Desarrollo y DevOps**: Azure DevOps, Azure App Service y Azure DevTest Labs son herramientas clave para el desarrollo y la entrega de aplicaciones.
- **Seguridad**: Azure Active Directory, Azure Security Center y Azure Key Vault son servicios destacados en este campo.

## Componentes

<p align="center">
  <img src="https://editor.analyticsvidhya.com/uploads/43045azure_services.png"/>
</p>

- **Azure Resource Manager (ARM)**: Facilita la administración y organización de recursos en Azure mediante grupos de recursos.
- **Azure Virtual Machines (VMs)**: Permite la creación de máquinas virtuales con diferentes sistemas operativos.
- **Azure Blob Storage**: Ofrece almacenamiento de objetos de gran capacidad, adecuado para datos no estructurados.
- **Azure SQL Database**: Una base de datos relacional administrada en la nube.
- **Azure Active Directory (AD)**: Un servicio de identidad y acceso para aplicaciones en la nube.
- **Azure Functions**: Permite ejecutar código sin servidor en respuesta a eventos.
- **Azure Kubernetes Service (AKS)**: Facilita la administración de clústeres de contenedores mediante Kubernetes.
- **Azure Cosmos DB**: Una base de datos de varios modelos y globalmente distribuida.

## Caracteristicas de seguridad

- **Centro de Confianza Global**: Azure opera con centros de datos seguros y cumple con estándares de seguridad y cumplimiento globalmente reconocidos.
- **Cumplimiento y Certificaciones**: Certificaciones de cumplimiento con estándares como ISO 27001, SOC 1, SOC 2, HIPAA, entre otros, asegurando que los servicios cumplan con requisitos regulatorios.
- **Gestión de Identidad y Acceso**: Azure Active Directory proporciona autenticación y control de acceso basado en roles para usuarios y recursos.
- **Seguridad en Redes**: Con Azure Network Security, se puede implementar firewalls, grupos de seguridad de red y herramientas de monitoreo para proteger el tráfico de red.
- **Gestión de Claves y Cifrado**: Azure Key Vault permite la gestión segura de claves, secretos y certificados, mientras que el cifrado de datos en reposo y en tránsito se puede lograr con Azure Storage Encryption y Azure SSL/TLS.
- **Seguridad en Capas**: La arquitectura de seguridad en capas permite implementar defensas en profundidad, protegiendo desde el perímetro hasta los datos.

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1400/1*IzhC5MFEEXUtkclep7Lx_g.png"/>
</p>

## Servicios de seguridad

<p align="center">
  <img src="https://techcommunity.microsoft.com/t5/image/serverpage/image-id/256459i5FA890E666D3F0CD/image-size/large?v=v2&px=999"/>
</p>

- **Azure Security Center**: Proporciona visibilidad y control continuo sobre el estado de seguridad de los recursos en la nube, además de ofrecer recomendaciones para mejorar la postura de seguridad.
- **Azure Sentinel**: Es un servicio de SIEM (Gestión de Eventos e Información de Seguridad) que ofrece inteligencia de seguridad avanzada para detectar y responder a amenazas.
- **Azure Active Directory Identity Protection**: Detecta, investiga y responde a amenazas identificando y proporcionando informes sobre riesgos de identidad y acceso.
- **Azure Information Protection**: Permite clasificar y proteger documentos y correos electrónicos mediante etiquetas de seguridad y control de acceso.
- **Azure Firewall**: Ofrece una protección de firewall de aplicación y red para recursos en la nube.

### Kusto Query Language (KQL) 

- Es el lenguaje de consulta utilizado en Microsoft Sentinel.
- Es altamente eficiente para consultas en tiempo real.
- Tiene una sintaxis similar a SQL, pero está optimizado para consultas de registros y datos de telemetría.

- Ejemplo Query

```
SecurityEvent
| where EventID == 4625
| summarize count() by Computer, Account
```

- Este ejemplo consulta los eventos de seguridad y filtra aquellos con el EventID 4625 (intentos fallidos de inicio de sesión), y luego resume el recuento por computadora y cuenta de usuario.
- La combinación de Sentinel y KQL ofrece a los equipos de seguridad una herramienta poderosa para detectar amenazas y responder a incidentes de manera eficiente.

<p align="center">
  <img src="https://mountainss.files.wordpress.com/2021/04/security-by-design.png"/>
</p>
