# Amazon Web Services

## Importancia del cómputo en la nube

- Escalabilidad
- Ahorro de costos
- Flexibilidad
- Productividad incrementada

## Servicios AWS

### [Amazon Elastic Compute Cloud (EC2)](https://aws.amazon.com/es/ec2/)

- Permite a los usuarios alquilar capacidad informática virtual.
- Se puede crear y gestionar servidores virtuales (llamados instancias) según las necesidades.
- Permite escalar la capacidad computacional hacia arriba o hacia abajo según la demanda.
- Se factura por el tiempo que se utilizan las instancias.
- Permite ejecutar una amplia gama de sistemas operativos y software en las instancias.
- Proporciona herramientas para configurar redes privadas virtuales (VPN), firewalls y control de acceso para mantener los datos seguros.
 
### [Amazon Machine Images (AMI)](https://docs.aws.amazon.com/es_es/AWSEC2/latest/UserGuide/AMIs.html)

- Se utiliza para crear y lanzar instancias de máquinas virtuales en AWS.
- Es una plantilla que contiene una imagen preconfigurada de un sistema operativo, aplicaciones y configuraciones predeterminadas.
- Facilitar la implementación rápida y consistente de entornos informáticos dentro de la infraestructura de AWS.
- Permiten a los usuarios crear copias de máquinas virtuales (instancias EC2) de manera eficiente.
 
### [AWS Lambda](https://aws.amazon.com/es/lambda/)

- Es un servicio de cómputo sin servidor que permite ejecutar código sin la necesidad de aprovisionar o administrar servidores.
- Ejecutar tareas automatizadas, como procesar archivos o realizar copias de seguridad.
- Es excelente para responder a eventos en tiempo real.
- Construir aplicaciones web sin servidor.
- Se puede emplear para procesar flujos de datos en tiempo real, como análisis de registros o generación de métricas en tiempo real.
- Enviar notificaciones o alertas basadas en ciertos eventos o condiciones en tus aplicaciones.
- Procesamiento de datos de dispositivos IoT.

## Servicios de contenedores en AWS

### [Amazon Elastic Container Service (ECS)](https://aws.amazon.com/es/ecs/)

- Permite ejecutar y escalar contenedores Docker en AWS.
- Administra clústeres de contenedores sin la necesidad de configurar la infraestructura subyacente.

### [Amazon Elastic Container Registry (ECR)](https://aws.amazon.com/es/ecr/)

- Proporciona un repositorio privado para almacenar, administrar y compartir imágenes de contenedores Docker.
- Complementa servicios como ECS y EKS para facilitar el flujo de trabajo de desarrollo y despliegue.
  
### [Amazon Elastic Kubernetes Service (EKS)](https://aws.amazon.com/es/eks/)

- Proporciona un servicio gestionado para ejecutar Kubernetes en AWS.
- Simplifica la implementación, la escalabilidad y la gestión de aplicaciones basadas en Kubernetes.

## Componentes AWS Cloud Infrastructure

![Imagen](https://i.imgur.com/vS9FE77.png)

### Administración y supervisión

- [**AWS CloudWatch**](https://aws.amazon.com/es/cloudwatch/): Ofrece monitoreo y observabilidad para recursos en la nube, permitiendo la recopilación de registros, seguimiento de métricas, creación de alarmas y visualización de datos operativos en tiempo real.

- [**AWS CloudTrail**](https://aws.amazon.com/es/cloudtrail/): Registra todas las acciones realizadas en una cuenta de AWS, lo que permite el seguimiento de cambios, el cumplimiento de auditorías y la solución de problemas operativos.

- [**AWS Config**](https://aws.amazon.com/es/config/): Facilita la evaluación y el seguimiento continuo de la configuración de los recursos de AWS. Permite mantener un registro de la configuración histórica y establecer reglas para garantizar la conformidad con las mejores prácticas.

- [**AWS Systems Manager**](https://docs.aws.amazon.com/es_es/systems-manager/latest/userguide/what-is-systems-manager.html): Proporciona una vista unificada de los recursos de AWS, permitiendo la automatización de tareas de administración, como la configuración, la administración de parches, la automatización de tareas y la creación de inventarios.

- [**AWS Trusted Advisor**](https://aws.amazon.com/es/premiumsupport/technology/trusted-advisor/): Ofrece recomendaciones para optimizar los recursos de AWS, mejorar la seguridad, reducir costos y mejorar el rendimiento.

- [**AWS Organizations**](https://aws.amazon.com/es/organizations/): Facilita la administración de múltiples cuentas de AWS, permitiendo la creación de políticas, la consolidación de facturación y el control centralizado.

### Bases de datos

- [**Amazon RDS (Relational Database Service)**](https://aws.amazon.com/es/rds/): Ofrece bases de datos relacionales como MySQL, PostgreSQL, SQL Server, Oracle, y MariaDB. Gestiona tareas como aprovisionamiento, parches, copias de seguridad y recuperación.

- [**Amazon DynamoDB**](https://aws.amazon.com/es/dynamodb/): Una base de datos NoSQL totalmente administrada y escalable que ofrece un rendimiento rápido y predecible con latencia baja.

- [**Amazon Redshift**](https://aws.amazon.com/es/redshift/): Es un servicio de almacenamiento de datos completamente administrado y almacén de datos de petabytes que se integra con la infraestructura existente y herramientas de BI (Business Intelligence).

- [**Amazon DocumentDB**](https://aws.amazon.com/es/documentdb/): Compatible con MongoDB, es una base de datos de documentos rápida, escalable y altamente disponible.

- [**Amazon Aurora**](https://aws.amazon.com/es/rds/aurora/): Un motor de base de datos relacional compatible con MySQL y PostgreSQL, que ofrece un rendimiento hasta cinco veces mejor que estos motores.

- [**Amazon Neptune**](https://aws.amazon.com/es/neptune/): Un servicio de base de datos gráfica rápido, confiable y completamente administrado, que facilita la creación y ejecución de aplicaciones que trabajan con datos altamente conectados.

- [**Amazon Timestream**](https://aws.amazon.com/es/timestream/): Un servicio de base de datos para series temporales, optimizado para almacenar y consultar datos de series temporales.

### Redes

- [**Amazon VPC (Virtual Private Cloud)**](https://aws.amazon.com/es/vpc/): Permite a los usuarios crear una red virtual personalizada en el entorno de AWS. Ofrece control sobre la configuración de la red, como la asignación de direcciones IP, la creación de subredes y la gestión de tablas de ruteo.

- [**Amazon Route 53**](https://aws.amazon.com/es/route53/): Es el servicio de DNS de AWS, proporcionando escalabilidad y disponibilidad para conectar las solicitudes de usuarios de internet con los recursos de AWS.

- [**AWS Direct Connect**](https://aws.amazon.com/es/directconnect/): Ofrece conexiones dedicadas desde el centro de datos del usuario a la nube de AWS, proporcionando una conexión más consistente y rápida que a través de la internet pública.

- [**AWS Transit Gateway**](https://aws.amazon.com/es/transit-gateway/): Simplifica la conectividad entre redes en entornos de múltiples cuentas y regiones, facilitando la administración de redes.

- [**AWS CloudFront**](https://aws.amazon.com/es/cloudfront/): Como servicio de CDN (Content Delivery Network), distribuye contenido web y datos de forma rápida y segura a los usuarios finales.

- [**AWS VPN**](https://aws.amazon.com/es/vpn/): Permite extender la red local hacia la nube de AWS de manera segura mediante conexiones cifradas.

- [**AWS Elastic Load Balancing**](https://aws.amazon.com/es/elasticloadbalancing/): Distribuye automáticamente el tráfico entrante de aplicaciones entre diversos destinos, como instancias EC2, mejorando la tolerancia a fallos y la escalabilidad.

### Cómputo

- [**AWS Batch**](https://aws.amazon.com/es/batch/): Se emplea para ejecutar trabajos en paralelo de alto rendimiento, liberando a los usuarios de la carga de administrar la infraestructura subyacente.

- [**Amazon Lightsail**](https://aws.amazon.com/es/lightsail/): Ofrece servidores virtuales, bases de datos, almacenamiento y redes de fácil utilización y coste reducido, siendo una opción ideal para aplicaciones más simples o para usuarios menos experimentados en la nube.

### Serverless

- [**AWS Lambda**](https://aws.amazon.com/es/lambda/): Permite ejecutar código sin servidor, escalando automáticamente en respuesta a eventos definidos. Los desarrolladores solo necesitan cargar su código y AWS se encarga del resto.

- [**Amazon API Gateway**](https://aws.amazon.com/es/api-gateway/): Facilita la creación, publicación, mantenimiento y protección de API para aplicaciones. Ofrece integraciones con AWS Lambda para construir fácilmente API serverless.

- [**AWS Step Functions**](https://aws.amazon.com/es/step-functions/): Ayuda a coordinar componentes de aplicaciones serverless mediante flujos de trabajo visuales. Permite la creación de flujos de trabajo que coordinan servicios como Lambda Functions.

### Recuperación ante desastres

- [**AWS Backup**](https://aws.amazon.com/es/backup/): Servicio gestionado para centralizar y automatizar copias de seguridad de múltiples servicios de AWS.
 
- [**AWS Elastic Disaster Recovery**](https://aws.amazon.com/es/disaster-recovery/): Recuperación de aplicaciones escalable y rentable en AWS.

### Almacenamiento

- [**Amazon S3 (Simple Storage Service)**](https://aws.amazon.com/es/s3/): Es uno de los servicios de almacenamiento en la nube más populares, permitiendo almacenar y recuperar datos de manera flexible y escalable con altos niveles de durabilidad.

- [**Amazon EBS (Elastic Block Store)**](https://aws.amazon.com/es/ebs/): Proporciona almacenamiento de bloques persistente para instancias de EC2.

- [**Amazon Glacier**](https://aws.amazon.com/es/s3/storage-classes/glacier/): Diseñado para el almacenamiento de datos a largo plazo y archivado. Ofrece un costo más bajo que S3 pero con tiempos de acceso más largos, ideal para datos a los que se accede con poca frecuencia.

- [**Amazon EFS (Elastic File System)**](https://aws.amazon.com/es/efs/): Proporciona un sistema de archivos escalable y completamente administrado para usar con instancias de EC2 y servicios locales. Permite el acceso simultáneo desde múltiples instancias de EC2.

### Seguridad y control de acceso

- [**Identity and Access Management (IAM)**](https://aws.amazon.com/es/iam/): IAM permite la gestión centralizada de usuarios, roles y permisos, controlando quién puede acceder a los recursos y qué acciones pueden realizar.

- [**AWS Identity Federation**](https://aws.amazon.com/es/identity/federation/): Proporciona un método seguro para acceder a los recursos de AWS a través de servicios de identidad existentes, como Microsoft Active Directory.

- [**AWS Key Management Service (KMS)**](https://aws.amazon.com/es/kms/): Facilita la creación y gestión de claves de cifrado para proteger datos y recursos sensibles.

- [**AWS WAF (Web Application Firewall)**](https://aws.amazon.com/es/waf/): Ofrece una capa adicional de seguridad para las aplicaciones web, filtrando el tráfico malicioso y protegiendo contra ataques comunes.

- [**AWS Shield**](https://aws.amazon.com/es/waf/): Brinda protección contra ataques de denegación de servicio distribuido (DDoS) para aplicaciones y recursos alojados en AWS.

- [**Amazon Inspector**](https://aws.amazon.com/es/inspector/): Realiza evaluaciones automatizadas de seguridad para identificar posibles vulnerabilidades en las aplicaciones desplegadas en AWS.

- [**Amazon GuardDuty**](https://aws.amazon.com/es/guardduty/): Monitorea y analiza continuamente la actividad maliciosa en una cuenta de AWS, proporcionando detección de amenazas.

### Inteligencia Artificial y Machine Learning

- [**Amazon SageMaker**](https://aws.amazon.com/es/sagemaker/): Plataforma para construir, entrenar y desplegar modelos de ML.
- [**Amazon Rekognition**](https://aws.amazon.com/es/rekognition/): Reconocimiento de imágenes y videos.
- [**Amazon Comprehend**](https://aws.amazon.com/es/comprehend/): Procesamiento de lenguaje natural (NLP) para análisis de texto.
- [**Amazon Polly**](https://aws.amazon.com/es/polly/): Conversión de texto a voz (TTS).
- [**Amazon Lex**](https://aws.amazon.com/es/pm/lex/): Creación de interfaces de conversación (chatbots).

## AWS Storage

## AWS Networking

- Grupos de seguridad, ACL
- Direcciones IP
- VPC
- Subredes
- LB y ELB
- Internet Gateway (IGW)
  
## Identities and Secure Access

- IAM (usuarios IAM, usuario raiz, grupos, funciones)
- Directivas de IAM
- Usuarios de terceros (ldp) (Amazon Cognito, AD)

## Monitoring and Management

- Supervisión
- CloudTrail
- Monitorización EC2
- CloudWatch

 ## CloudFormation

 - Ejemplo de una plantilla
 - Pros y contras
