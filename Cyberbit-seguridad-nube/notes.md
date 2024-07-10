# Curso de Seguridad en la Nube e Inteligencia de Amenazas

## Descripción

Aprovechar los recursos en la nube en redes híbridas o totalmente basadas en la nube introduce nuevos riesgos para la organización. A lo largo de este curso, los estudiantes adquirirán una comprensión integral de las tecnologías en la nube con un enfoque en AWS y Azure. Además, familiarizará a los estudiantes con Docker, Kubernetes, el Círculo de Inteligencia de Amenazas, prácticas forenses y proporcionará amplios conocimientos sobre temas significativos en ciberseguridad, evaluaciones técnicas y tácticas defensivas para protegerse contra posibles amenazas.

## **Índice**

1. [Fundamentos AWS](#id1)
2. [Fundamentos Azure](#id2)
3. [Security+](#id3)
4. [Docker](#id4)
5. [Kubernetes](#id5)
6. [Vulnerabilidades](#id6)
7. [Malware](#id7)
8. [Actores de amenazas](#id8)
9. [Inteligencia de amenazas](#id9)
10. [Red Team](#id10)
11. [Blue Team](#id11)
12. [Agradecimientos](#id12)

## Fundamentos AWS<a name="id1"></a>

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

<p align="center">
  <img src="https://k21academy.com/wp-content/uploads/2020/08/type-of-storage.png"/>
</p>

## AWS Networking

- **Aspectos generales**
  + AWS Networking permite configurar reglas de enrutamiento para dirigir el tráfico dentro y fuera de la VPC.
  + Se pueden implementar configuraciones redundantes y escalables para asegurar alta disponibilidad.
  + Los mecanismos como grupos de seguridad, ACL y configuraciones de VPC permiten un control sobre la seguridad y el acceso a los recursos de red.
    
- **Grupos de Seguridad**
  + Funcionan a nivel de instancia EC2 y actúan como cortafuegos virtuales.
  + Permiten definir reglas de tráfico entrante y saliente basadas en puertos, protocolos y direcciones IP.

- **Listas de Control de Acceso (ACL)**
  + Se aplican a los subnets de una VPC y actúan como filtros de tráfico para controlar el acceso.
  + Permiten definir reglas para permitir o denegar tráfico basado en direcciones IP o rangos de puertos.

- **Direcciones IP**
  + Las instancias EC2 tienen direcciones IP privadas (dentro de la VPC) y públicas (para acceso desde internet).
  + AWS asigna direcciones IP automáticamente o puedes tener direcciones IP elásticas para persistencia.
 
- **VPC (Virtual Private Cloud)**
  + Es un entorno de red virtual aislado y configurable en AWS.
  + Permite definir rangos de direcciones IP, subredes, tablas de ruteo y gateways para las instancias desplegadas.
  + Las subredes dividen una VPC en segmentos más pequeños con su propio rango de direcciones IP.

- **Load Balancing (LB)**
  + Distribuye el tráfico de red entre varias instancias EC2 para mejorar la disponibilidad y la escalabilidad.
  + Equilibra la carga para asegurar un uso uniforme de recursos.

- **Elastic Load Balancing (ELB)**
  + Un servicio de AWS que proporciona balanceo de carga automáticamente y de forma escalable.
  + Hay tres tipos: Classic Load Balancer, Application Load Balancer y Network Load Balancer, cada uno con diferentes funcionalidades y usos.

- **Internet Gateway (IGW)**
  + Permite la comunicación entre una VPC y el internet público.
  + Proporciona una ruta para el tráfico entrante y saliente hacia y desde la VPC.

<p align="center">
  <img src="https://d1.awsstatic.com/getting-started-guides/vpc-with-nat.7ad78b23ba91be288afdf8a0d836820add439d44.png"/>
</p>

## Identities and Secure Access

- **Aspectos generales**
  + IAM proporciona una capa de seguridad crucial al controlar el acceso a los recursos de AWS.
  + Facilita la administración centralizada de identidades y permisos.
  + IAM permite el seguimiento de actividades y eventos a través de logs para identificar y revisar cambios o intentos de acceso no autorizados.
  + Puede integrarse con servicios de identidad existentes y ofrece flexibilidad para asignar y revocar permisos según sea necesario.

- **Usuarios IAM**
  + Representan personas o servicios que interactúan con AWS.
  + Cada usuario tiene credenciales únicas y asignación de permisos.

- **Usuario raiz**
  + Es el primer usuario creado al configurar una cuenta de AWS.
  + Tiene acceso completo a todos los recursos y servicios de la cuenta.

- **Grupos**
  + Permiten agrupar usuarios para asignarles políticas comunes.
  + Simplifican la administración de permisos al asignar políticas de grupo en lugar de individualmente a cada usuario.

- **Funciones**
  + Son entidades que definen roles temporales para usuarios, aplicaciones o servicios.
  + Se utilizan para delegar permisos de manera temporal o dentro de un servicio.
 
- **Control de acceso granular**
  + Son documentos JSON que definen qué acciones pueden realizar los usuarios y sobre qué recursos.
  + Permiten especificar condiciones para controlar el acceso más detalladamente.
  + Se aplican a usuarios, grupos o roles.

- **Amazon Cognito**
  + Un servicio que gestiona la autenticación, autorización y administración de usuarios para aplicaciones web y móviles.
  + Permite la autenticación con proveedores de identidad externos (como Google, Facebook).

- **Active Directory**
  + Puede integrarse con AWS para permitir la gestión de identidades desde un directorio activo existente.
  + Permite la federación de identidades entre el directorio AD local y los servicios de AWS.

<p align="center">
  <img src="https://digitalcloud.training/wp-content/uploads/2022/01/IAM-1.jpg"/>
</p>

## Monitoring and Management

- **Supervisión en AWS**
  + AWS ofrece herramientas para supervisar el rendimiento y el estado de los recursos en tiempo real.
  + Esto incluye monitoreo de instancias EC2, almacenamiento, bases de datos y más.
    
- ** AWS CloudTrail**
  + CloudTrail realiza un seguimiento de las actividades y acciones realizadas dentro de una cuenta de AWS.
  + Registra eventos como creación de recursos, cambios de configuración y accesos a recursos.
  + Ayuda en la auditoría y el cumplimiento de normativas al proporcionar un registro detallado de actividades.
    
- **Monitorización EC2**
  + Permite monitorear el estado de las instancias EC2, incluyendo CPU, memoria, red, etc.
  + Proporciona métricas detalladas sobre el rendimiento de las instancias.
    
- ** Amazon CloudWatch**
  + CloudWatch ofrece monitoreo y alertas para recursos y aplicaciones en AWS.
  + Permite crear dashboards personalizados para visualizar métricas y eventos clave.
  + Permite configurar alarmas para responder a cambios en las métricas (por ejemplo, aumentar la capacidad si la carga aumenta).
  + Integra el autoescalado para ajustar automáticamente la capacidad en función de las métricas de CloudWatch.

 ## CloudFormation

- CloudFormation es una herramienta poderosa para definir y gestionar infraestructura en AWS de manera automatizada y controlada.
- CloudFormation permite realizar cambios en la infraestructura existente de manera controlada y predecible, facilitando las actualizaciones.
- Permite la reutilización de plantillas y la creación de plantillas anidadas para una gestión más modular y escalable de la infraestructura.
- Se integra bien con herramientas de automatización y despliegue continuo (CI/CD), facilitando el despliegue de infraestructura como parte de un flujo de trabajo de DevOps.
   
- **Plantilla de ejemplo**

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "Ejemplo de una plantilla de CloudFormation",
   "Resources": {
      "MyEC2Instance": {
         "Type": "AWS::EC2::Instance",
         "Properties": {
            "ImageId": "ami-12345678",
            "InstanceType": "t2.micro"
         }
      },
      "MyS3Bucket": {
         "Type": "AWS::S3::Bucket",
         "Properties": {
            "BucketName": "mi-bucket-s3"
         }
      }
   }
}
```

- Permite la definición y despliegue automatizado de recursos en AWS mediante código.
- Facilita la gestión y el control de la infraestructura como código, lo que simplifica la replicabilidad y el control de versiones.
- Gestiona las relaciones y dependencias entre los recursos, asegurando un despliegue coherente y ordenado.
- Puede requerir tiempo para dominar la creación de plantillas complejas.
- Algunas configuraciones avanzadas pueden ser complicadas de manejar o no están disponibles directamente en CloudFormation

<p align="center">
  <img src="https://docs.aws.amazon.com/images/AWSCloudFormation/latest/UserGuide/images/update-stack-diagram.png"/>
</p>

## Riesgos AWS Lambda

- **Inyección de Código Malicioso**
  + Escenario: Un atacante intenta inyectar código malicioso en la función Lambda para obtener acceso no autorizado o realizar acciones destructivas.
  + Ejemplo: Un payload manipulado se introduce en la función Lambda, lo que permite ejecutar comandos no autorizados en el entorno de ejecución.

- **Privilegios Excesivos o Inadecuados**
  + Escenario: Configuración incorrecta de permisos en la función Lambda que otorgan más privilegios de los necesarios.
  + Ejemplo: La función Lambda tiene acceso a recursos sensibles como bases de datos o almacenamiento, lo que podría comprometer datos confidenciales si se ve comprometida.
    
- **Fugas de Información Sensible**
  + Escenario: La función Lambda maneja datos confidenciales sin la debida protección.
  + Ejemplo: Una función Lambda mal configurada imprime información sensible en logs, exponiendo inadvertidamente datos como contraseñas o claves de API.

- **Ataques de Denegación de Servicio (DDoS)**
  + Escenario: Una función Lambda mal diseñada podría ser vulnerable a ataques que sobrecarguen su capacidad de manejar solicitudes.
  + Ejemplo: Un atacante envía un gran volumen de solicitudes a una función Lambda, lo que provoca una saturación y una interrupción en el servicio.

- **Vulnerabilidades en Dependencias**
  + Escenario: Uso de librerías o dependencias no actualizadas o con vulnerabilidades conocidas.
  + Ejemplo: Una función Lambda utiliza una biblioteca de terceros con una vulnerabilidad conocida que permite a un atacante explotar la función.
    
- **Ejecución de código sin Supervisión**
  + Escenario: Falta de monitoreo adecuado sobre las funciones Lambda en producción.
  + Ejemplo: Una función Lambda mal optimizada consume recursos excesivos o se bloquea, lo que afecta otras funciones o servicios que dependen de ella.

- **Falta de Seguimiento y Auditoría**
  + Escenario: Ausencia de registros (logs) o auditoría sobre las acciones realizadas por las funciones Lambda.
  + Ejemplo: Una función Lambda comprometida realiza acciones sin dejar rastro, dificultando la identificación del origen del ataque.

- **Manipulación de Entrada**
  + Escenario: Falta de validación de entradas en las funciones Lambda, lo que permite la manipulación de datos.
  + Ejemplo: Un atacante manipula los datos de entrada para sobrecargar la función o causar un comportamiento inesperado.

- **Escenario Black Box**

<p align="center">
  <img src="https://sysdig.com/wp-content/uploads/vuln_lambda_mitre_03-1.png"/>
</p>

- El atacante encuentra un cubo S3 mal configurado con archivos de la empresa expuestos públicamente.
- Usando una función Lambda desconocida, el atacante sube archivos y encuentra etiquetas dinámicas.
- Realiza pruebas cargando archivos para observar la adición automática de etiquetas.
- Manipula nombres de archivos para ejecutar comandos remotos en la función Lambda.
- Aprovecha la falta de validación para extraer credenciales de AWS.
- Utiliza las credenciales obtenidas para acceder y evaluar privilegios dentro de la cuenta en la nube.
  
- **Escenario White Box**

<p align="center">
  <img src="https://sysdig.com/wp-content/uploads/vuln_lambda_mitre_05-1-2.png"/>
</p>

- El atacante accede al entorno en la nube mediante credenciales robadas por phishing.
- El usuario comprometido tiene acceso de solo lectura en la cuenta.
- Se verifica la validez de las credenciales y se evalúan los privilegios del usuario comprometido.
- Al tener solo acceso de lectura, se recolecta información sobre los recursos existentes, enfocándose en el cubo S3 mal configurado.
- Se asume la presencia de una función Lambda para el cubo S3 encontrado. Se busca más información sobre esta función.
- Se identifica la función "corpFuncEasy" y se accede a detalles críticos, incluyendo el código fuente.
- Se descubre que el código no valida correctamente los nombres de archivo, lo que lleva a una vulnerabilidad.
- Aprovechando la falta de validación, se insertan comandos adicionales en el nombre de archivo, ejecutando comandos maliciosos con éxito.

- **Medidas de mitigación**
  + Limitar el acceso público al bucket S3, restringiéndolo a usuarios autenticados dentro de la cuenta de AWS para evitar accesos no deseados.
  + Asegurarse de que el código implementado en la función Lambda siga las mejores prácticas de seguridad para evitar vulnerabilidades.
  + Validar la entrada de usuario para prevenir la ejecución de comandos maliciosos.
  + Utilizar IAM para asignar permisos de acceso precisos y limitados a los recursos de AWS, reduciendo las posibles rutas de escalada de privilegios.


## Fundamentos Azure<a name="id2"></a>

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


## Security+<a name="id3"></a>

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


## Docker<a name="id4"></a>

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


## Kubernetes<a name="id5"></a>

## Aspectos generales

- Kubernetes fue desarrollado por Google para ayudar en la gestión de aplicaciones en entornos de contenedores.
- Facilitar la administración de aplicaciones distribuidas y su despliegue en múltiples hosts de manera eficiente y escalable.
- Administra contenedores de manera eficiente, garantizando su escalabilidad, disponibilidad y automatización.
- Permite definir y automatizar la configuración de la infraestructura y las políticas de despliegue.

<p align="center">
  <img src="https://www.cncf.io/wp-content/uploads/2020/08/Kubernetes-architecture-diagram-1-1.png"/>
</p>

## **Componentes**
  - **Node**: La máquina física o virtual que ejecuta los contenedores. Cada nodo tiene agentes para administrar los contenedores.
  - **Cluster**: Conjunto de nodos que ejecutan aplicaciones Kubernetes.
  - **Master**: Coordina el cluster y sus operaciones.
  - **Kubelet**: Agente que ejecuta en cada nodo del cluster y se encarga de la gestión de los contenedores en ese nodo.
  - **Control Plane**: Componente central que gestiona el cluster. Incluye el API Server, el Scheduler, el Controller Manager y el etcd.
  - **Etcd**: Almacena los datos de configuración y estado del cluster Kubernetes.
  - **API Server**: Expone la API de Kubernetes y es el punto de entrada para administrar el cluster.
  - **Scheduler**: Asigna los contenedores a los nodos disponibles en función de los recursos y restricciones.
  - **Controller Manager**: Controla los controladores que regulan el estado del cluster.

## **Comando básicos**

| Comando                                                      | Descripción                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `kubectl create`| Crea recursos definidos en un archivo YAML |
| `kubectl apply`  | Aplica cambios en la configuración de los recursos |
| `kubectl get` | Obtiene información sobre recursos (pods, servicios, nodos, etc |
| `kubectl describe`   | Muestra detalles específicos sobre un recurso |
| `kubectl delete`  | Elimina recursos |


## Vulnerabilidades<a name="id6"></a>

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


## Malware<a name="id7"></a>

## CronRAT 

- Es un malware avanzado que se oculta en el sistema de calendario de Linux el día 31 de febrero, que no existe.
- es un malware de tipo troyano de acceso remoto (RAT), estos permiten a los atacantes tomar el control remoto.
- Esto lo hace difícil de detectar para las soluciones de seguridad tradicionales.
- Se utiliza para robar datos de los servidores de comercio electrónico.
- CronRAT se oculta en el sistema de calendario y espera a recibir instrucciones del atacante.
- Adquirir acceso remoto al servidor de comercio electrónico y robar datos de los clientes.
- Los datos robados pueden utilizarse para cometer fraude, robo de identidad y otros delitos.
- Realizar escaneos de seguridad regulares para detectar malware.
- Actualizar sus sistemas de seguridad para proteger contra las vulnerabilidades que CronRAT explota.

## DarkWatchman RAT

- Es un malware tipo RAT que se distribuye a través de correos electrónicos de phishing con archivos ZIP adjuntos.
- Está escrito en JavaScript y C#.
- Está dirigido principalmente a organizaciones rusas.
- Se oculta en el registro de Windows para evitar ser detectado por las soluciones antivirus.
- Los usuarios deben estar atentos a los correos phishing y evitar abrir archivos adjuntos de fuentes desconocidas.

## Qakbot

- Es un malware modular y sofisticado que se ha utilizado para una variedad de propósitos maliciosos.
- Qakbot puede propagarse a otros sistemas en la misma red a través de una variedad de métodos.
- Se ha utilizado para distribuir ransomware, como REvil, Egregor y Black Basta.
- El malware puede robar datos confidenciales de las víctimas, contraseñas y claves de cifrado.
- También puede usarse para tomar el control remoto de sistemas comprometidos.
- Se propaga comúnmente a través de correos electrónicos de phishing que contienen enlaces o archivos adjuntos maliciosos.
- Ha sido utilizado para robar información confidencial, propagar ransomware y tomar el control remoto. 

## Zloader

- Es un malware de tipo troyano bancario que se utiliza para robar datos sensibles, como contraseñas y tarjetas de crédito.
- Es una variante del troyano Zeus, uno de los malware más populares y peligrosos de la historia.
- utiliza una variedad de técnicas para evadir la detección de los sistemas de seguridad, como la ofuscación, el cifrado y el uso de técnicas de carga dinámica.
- También se ha utilizado para distribuir ransomware, como Egregor y Ryuk.
- se puede utilizar para crear una botnet, que es una red de dispositivos infectados controlados remotamente.
  
## Sysjoker - Cross-Platform FUD Backdoor

- Es un malware backdoor multiplataforma que fue descubierto por primera vez en diciembre de 2021 por Intezer.
- Está escrito en C++ y tiene variantes para Linux, Windows y macOS.
- Se disfraza como una actualización del sistema.
- Recupera las direcciones del servidor C2 de un archivo de texto alojado en Google Drive.
- Crea una entrada de registro para iniciarse automáticamente al iniciar Windows.
- Recopila información del sistema, como la versión de Windows, el nombre de usuario y la dirección MAC.
- El atacante puede controlar el malware a través del servidor C2 y ejecutar comandos en el sistema infectado.
- Se ha vinculado a ataques dirigidos por un actor relacionado con Hamas durante el conflicto Israel-Hamas de 2022.

## FritzFrog

- No se almacena en el disco duro de la víctima, sino que se ejecuta en la memoria. Esto dificulta su detección y eliminación.
- Puede ejecutar múltiples procesos simultáneamente, lo que lo hace más eficiente.
- Utiliza una arquitectura P2P para comunicarse entre los nodos infectados.
- Se propaga principalmente a través de ataques de fuerza bruta contra servidores SSH.
- una vez que FritzFrog infecta un servidor, lo usa para minar criptomonedas, como Monero.
- FritzFrog también se puede usar para lanzar ataques DDoS.

## Hermetic Wiper

- Es un malware destructivo diseñado para infiltrarse en dispositivos Windows.
- Hace inoperables los dispositivos mediante la destrucción de archivos, la corrupción del Master Boot Record (MBR) y la afectación de unidades físicas pertenecientes a organizaciones de Ucrania.
- Abusa de un controlador de partición de gestión legítimo, "empntdrv.sys".
- Enumera el MBR y todas las particiones de todas las unidades físicas conectadas al dispositivo Windows.
- Sobrescribe los primeros 512 bytes de cada MBR y partición que pueda encontrar.
- Crea un archivo de registro con información sobre el ataque.
- Utiliza una técnica de ofuscación para dificultar su detección.
- Hermetic Wiper se utilizó en los ataques cibernéticos contra Ucrania que tuvieron lugar el 23 de febrero de 2022.
- El malware se distribuyó a través de correos electrónicos de phishing que contenían archivos adjuntos maliciosos.
- Los ataques se dirigieron a organizaciones gubernamentales, militares y de infraestructura de Ucrania.
- Perjudicó la capacidad de las organizaciones para responder a la invasión rusa.
  
## Emotet

- Es un troyano bancario que se propaga principalmente a través de correos electrónicos de spam (malspam).
- Suelen contener archivos adjuntos maliciosos, como archivos de documentos habilitados para macros o enlaces maliciosos.
- El objetivo principal de Emotet es robar credenciales bancarias y otros datos sensibles.
- También puede ser utilizado para distribuir otros tipos de malware, como ransomware, troyanos de acceso remoto y bots.

## DirtyMoe

- Es un malware botnet modular diseñado para infectar sistemas Windows.
- Utiliza la potencia de procesamiento de las computadoras infectadas para minar criptomonedas.
- Puede ser utilizado para lanzar ataques DDoS contra sitios web o servicios.
- Está diseñado como un sistema modular, lo que significa que sus funciones se implementan como módulos separados.

## Denonia - First Malware on AWS Lambda

- Es un malware de tipo criptominero, es decir, que se utiliza para minar criptomonedas.
- Está escrito en Go, un lenguaje de programación de código abierto.
- Está diseñado para atacar entornos de AWS Lambda.
- Utiliza DNS over HTTPS (DoH) para comunicarse con su servidor de control y comando (C&C).
- Utiliza XMRig, un software de minería de Monero, para minar criptomonedas.
- Se cree que Denonia se distribuye a través de la explotación de claves de acceso y secretos de AWS.
- Los eventos de AWS Lambda pueden ser monitoreados para detectar actividad sospechosa.
- El código de Denonia puede ser identificado por su firma digital o por su comportamiento.

## Raspberry Robin

- Es un malware de tipo gusano que se propaga a través de dispositivos USB infectados.
- Fue descubierto por Red Canary en 2021.
- Se ha observado que se dirige a organizaciones de telecomunicaciones y gobiernos.

## Jester Stealer

- Es un malware de tipo infostealer que roba información sensible de los sistemas infectados.
- Fue descubierto por primera vez en julio de 2021.
- Se distribuye principalmente a través de correos electrónicos de phishing y archivos adjuntos infectados.
- El malware envía los datos robados a un servidor remoto controlado por el atacante.
- El malware usa un canal de comunicación cifrado para dificultar la detección.
- El malware detecta entornos de virtualización y se niega a ejecutarse en ellos.
- El malware usa funciones nativas del sistema operativo para evitar la detección por parte de las soluciones de seguridad.

## TrickBot

- Es un troyano bancario que busca robar credenciales bancarias y otras información confidencial.
- El método de infección es mediante spear phishingñ
- Los cibercriminales también pueden utilizar exploits para infectar dispositivos con TrickBot.
- Es un malware mutable, lo que significa que los criminales pueden modificarlo con regularidad para evitar la detección.
- Puede exfiltrar datos confidenciales de los dispositivos infectados.
  
## Conti

- Es un malware ransomware que cifra los archivos de la víctima y exige un rescate para su descifrado.
- Opera como un ransomware como servicio (RaaS)
- se distribuye a través de correo electrónico y enlaces maliciosos.
- Una vez que Conti se ejecuta en la computadora de la víctima, comienza a cifrar los archivos.
- Una vez que se completa el cifrado, Conti muestra un mensaje de rescate a la víctima.
- Conti es especialmente conocido por su uso de técnicas de extorsión doble.
- Además de cifrar los archivos de la víctima, también puede robar datos sensibles, como información financiera o personal.
- Si la víctima no paga el rescate, Conti amenaza con publicar los datos robados en línea.
- Entre las víctimas se incluyen empresas, gobiernos y organizaciones sin fines de lucro.

## Symbiote

- Es un malware de tipo rootkit, lo que significa que tiene privilegios elevados en el sistema.
- Fue descubierto en junio de 2022 y está diseñado para robar credenciales y proporcionar acceso remoto a los atacantes.
- Utiliza una variedad de técnicas para ocultarse de las herramientas de seguridad, como antivirus y EDR.
- El malware puede inyectarse en otros procesos o aplicaciones en ejecución.
- Puede capturar credenciales de usuarios y administradores.
- Puede reemplazar las funciones del sistema con sus propias versiones maliciosas.
- Puede modificar los registros del sistema para ocultar su presencia.

## Stiff#Bizon

- Es una campaña de malware dirigida a organizaciones de alto valor en varios países, incluidos Polonia y Rumania.
- La campaña está atribuida al grupo de ciberespionaje norcoreano APT37.
- La infección se produce a través de correos electrónicos de phishing que contienen un archivo adjunto malicioso.
- El archivo adjunto es un archivo de Word que contiene un enlace a un archivo de acceso directo (LNK).
- El malware se instala en el sistema y establece una conexión con el servidor de control y comando (C&C).
  
## Matanbuchus

- Es un malware de tipo ransomware que se propaga a través de correos electrónicos de phishing.
- Matanbuchus cifra los archivos del usuario utilizando un algoritmo de cifrado AES-256.
- Cifra los archivos del usuario con una clave única. Esta clave se almacena en el sistema del usuario.
- La pantalla de rescate solicita un rescate en criptomonedas para descifrar los archivos.

## BluStealer

- Es un malware de tipo infostealer que se distribuye a través de correo electrónico con archivos adjuntos maliciosos.
- BluStealer puede robar una amplia gama de información personal y confidencial.
- Está escrito en Visual Basic 6.0, una tecnología obsoleta que puede dificultar su detección por parte de los AV.
- Utiliza técnicas de anti-virtualización para evitar ser ejecutado en máquinas virtuales.
- Archivos adjuntos maliciosos con nombres como "invoice.pdf", "receipt.docx", "statement.xlsx", etc.
- Procesos con nombres como "ChromeRecovery.exe", "ThunderFox.exe", "a310logger.exe", etc.
  
## Magniber

- Ransomware de tipo locker.
- Fue identificado por primera vez en 2017.
- En 2022, comenzó a distribuirse a través de correos electrónicos de phishing que se hacían pasar por actualizaciones de software de Microsoft.
- Una vez que Magniber se ha instalado en el sistema de la víctima, comienza a cifrar los archivos.
- Magniber usa un algoritmo de cifrado fuerte que es difícil de descifrar sin la clave de descifrado.
- También puede eliminar las copias de seguridad de los archivos para dificultar la recuperación de los datos.
- Ofrece a las víctimas un descuento si pagan el rescate rápidamente.
 
## ChromeLoader

- Es un malware que se distribuye principalmente a través de descargas maliciosas de software pirata o crackeado.
- Una vez que el malware se ejecuta, instala una extensión maliciosa en el navegador de la víctima.
- Es un malware multiplataforma que puede infectar computadoras con Windows y macOS.
- Utiliza técnicas de ofuscación para dificultar su análisis y detección.
 
## Racoon Stealer V2

- Es un malware de tipo infostealer que se utiliza para robar información confidencial de la víctima.
- Los atacantes suelen distribuir Raccoon Stealer v2 en sitios web que ofrecen software pirateado o gratuito.
- los atacantes pueden enviar correos electrónicos de phishing que contienen archivos adjuntos infectados.
 
## RapperBot

- Es un malware de botnet de IoT que se dirige a servidores Linux a través de ataques de fuerza bruta SSH.
- Se basa en gran medida en el código fuente original de Mirai, pero tiene varias características distintivas.
- Puede utilizar una lista de credenciales predefinidas para intentar acceder a servidores SSH.
- Puede instalarse en el sistema afectado para preservar su persistencia.
- se utiliza principalmente para lanzar ataques DDoS. Sin embargo, también se puede utilizar robo de credenciales.
  
## MiMi Backdoor

- Es un troyano que se infiltra en la aplicación de mensajería instantánea MiMi, que es popular en China.
- El malware permite a los atacantes tomar el control remoto de los sistemas infectados y robar datos.
- El malware se distribuye a través de versiones maliciosas de los instaladores de MiMi.
- Una vez que el malware se ejecuta, descarga y ejecuta un backdoor llamado rshell.
- El rshell permite a los atacantes ejecutar comandos en el sistema infectado, así como recopilar información del sistema.
- Ha sido utilizado en ataques dirigidos a organizaciones en China, Taiwán y Filipinas.
- Está vinculado al grupo de amenazas chino APT27, también conocido como Emissary Panda.
  
## Azov

- Malware wiper, cuyo objetivo es destruir datos.
- Primera aparición fue en diciembre de 2022.
- Escrito manualmente en ensamblador.
- Escribe bloques de 666 bytes de ruido aleatorio.
- No pide rescate.
- Se cree que es un ataque de falsa bandera.
- Podría ser utilizado por actores estatales o privados.
- Es capaz de borrar datos de forma irreversible, incluso de los sistemas de recuperación.
- se distribuye a través de la botnet SmokeLoader, que se propaga a través de sitios web de piratería y cracks.

## YARA

- Es una herramienta de código abierto utilizada para la identificación y clasificación de malware basada en patrones.
- Permite a los analistas de seguridad crear reglas para detectar y categorizar malware.
- Facilita la identificación de amenazas conocidas y desconocidas.
- Los usuarios pueden crear reglas de YARA utilizando un lenguaje que describe patrones asociados con el malware.
- Las reglas están formadas por cadenas de texto, expresiones regulares y condiciones lógicas.
- Las reglas de YARA permiten identificar patrones específicos dentro de archivos binarios o de texto.
- Los patrones pueden ser bytes, strings, estructuras específicas o comportamientos particulares del malware.
- Puede adaptarse a diferentes tipos de amenazas y variaciones dentro de una misma familia de malware.
- **Identificación de un archivo específico por su firma**
```
rule detect_malware {
    strings:
        $magic = { 4D 5A 90 00 03 00 00 00 } // Firma del archivo
    condition:
        $magic at 0 // La firma se encuentra al principio del archivo
}
```
- **Detección de una cadena de texto asociada con un troyano bancario**
```
rule banking_trojan {
    strings:
        $trigger = "Your bank account has been compromised" wide ascii
    condition:
        $trigger
}
```
- **Identificación de una secuencia de comandos maliciosa de PowerShell**
```
rule malicious_powershell {
    strings:
        $malicious_script = /powershell\s+\$[a-zA-Z]{2}=\$/ nocase
    condition:
        $malicious_script
}
```
- **Detección de un exploit conocido en un archivo PDF**
```
rule detect_pdf_exploit {
    strings:
        $exploit_code = { 25 50 44 46 2D } // Firma de un exploit conocido en PDF
    condition:
        $exploit_code
}
```
- **Identificación de un comportamiento sospechoso en un archivo ejecutable**
```
rule suspicious_behavior {
    condition:
        uint16(0) == 0x5A4D and // Verificación de la firma MZ de un archivo ejecutable
        all of ($file at pe.entry_point)  // Análisis de la entrada del punto de inicio del PE
}
```


## Actores de amenazas<a name="id8"></a>

## APT35

- APT35, también conocido como Charming Kitten o Fósforo, ha estado presente desde 2014.
- Realizaron una campaña de espionaje a través de las redes sociales, una de las más sofisticadas, organizadas por actores iraníes.
- En 2019, apuntaron a instituciones académicas en EE. UU., Francia y el Medio Oriente.
- En 2020, se dirigieron a organizaciones de investigación médica en Israel y EE. UU.
- En 2021, abusaron de las vulnerabilidades del servidor Microsoft Exchange (ProxyShell).
- Charming Kitten atacó a investigadores médicos, particularmente en oncología, genética y neurología, usando phishing con temas sensibles.
- Han realizado campañas altamente dirigidas, como "BadBlood", utilizando temas sensibles como armas nucleares de Israel.
- Han atacado a periodistas y activistas que informan sobre temas en el Medio Oriente.
- Utilizan backdoors PowerShell como PowerLess Backdoor para ejecutar comandos.
- Explotaron la vulnerabilidad Log4Shell/Log4j en enero de 2022, aprovechando la situación antes de que las organizaciones parcharan sus sistemas afectados.
- Recientemente, se observó a Charming Kitten usando Hyperscrape para extraer correos electrónicos.
- Hyperscrape se utiliza para recolectar información de disidentes iraníes y se ha descubierto que descarga datos de Google TakeOut.
  
## Lockbit

<p align="center">
  <img src="https://media.licdn.com/dms/image/D5622AQHN8gs-3HFp1Q/feedshare-shrink_800/0/1698731494971?e=2147483647&v=beta&t=mI-oASPx21We5kAvtFkURHu0i0e-yRwLYcE_pmOoLaA"/>
</p>

- Responsable de más de un tercio de los ataques de ransomware entre la segunda mitad del año anterior y el primer trimestre de 2023.
- Surgió en septiembre de 2019 y se convirtió en el grupo más activo en 2022 tras la desaparición del grupo Conti.
- Más de 1500 registros de anuncios de víctimas en la plataforma SOCRadar y más de 300 víctimas anunciadas en el primer trimestre de 2023.
- Atento reportó una pérdida de $42.1 millones en 2021 debido a un ataque de LockBit, con $34.8 millones en pérdida de ingresos y $7.3 millones en gastos de mitigación.
- Capacidad para atacar sistemas Windows, Linux, VMware ESXi y posiblemente sistemas MacOS, ARM, FreeBSD, MIPS y SPARC.
- Utiliza Ransomware-as-a-Service (RaaS) desde enero de 2020, empleando tácticas como doble extorsión y reclutamiento de insiders.
- Borra archivos de registro y sombras de volumen, emplea encriptación híbrida AES y RSA.
- Enfoque en entidades gubernamentales, educativas y de emergencia.
- Ganancias aproximadas de $91 millones en EE. UU. desde 2020.
- Tipica operación de LockBit

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2023/04/lockbit-operation-scheme.png"/>
</p>
  
## Lazarus

- Lazarus Group es un grupo de ciberataque que se cree tiene vínculos con Corea del Norte.
- Se les ha atribuido una serie de operaciones cibernéticas desde principios de la década de 2000.
- Sus actividades están centradas en operaciones financieras fraudulentas.
- Utilizan malware personalizado, ataques de ingeniería social y técnicas de evasión.
- Han utilizado malware como "Trojan.Fastcash", diseñado específicamente para manipular sistemas de pagos internacionales.
- Ciclo de vida del ataque

<p align="center">
  <img src="https://hub.packtpub.com/wp-content/uploads/2018/10/APT38-Attack-Lifecycle.png"/>
</p>

- Han atacado instituciones financieras, criptomonedas y empresas de tecnología.
- Se estima que han robado más de 100 millones de dólares a través de sus ataques a diferentes instituciones financieras.
- Han llevado a cabo múltiples ataques notables, como el de WannaCry.
- Realizan una planificación previa a sus ataques, que pueden involucrar meses de vigilancia y reconocimiento de sus objetivos.

## Vice Society

- Vice Society surgió en 2021 y ha atacado organizaciones de todos los tamaños.
- Realizan cacería de grandes presas y emplean la táctica de doble extorsión: cifrado y robo de datos.
- A diferencia de otros grupos, no operan como un servicio de ransomware.
- Se cree que son una organización criminal con base en Rusia.
- En 2022, Vice Society fue el grupo más activo, con 39 ataques a la industria educativa.
- La educación fue una de las industrias más afectadas por el ransomware.
- Inicialmente, explotaban la vulnerabilidad PrintNightmare.
- Usaban ransomware de terceros, pero ahora han desarrollado su propio ransomware, "PolyVice".
- En diciembre de 2021, atacaron sistemas de operaciones de tiendas en el Reino Unido, cerrando muchas tiendas de Spar.
- En mayo de 2022, atacaron a Eskenazi Health en Indianápolis y al Waikato Region Health Board en Nueva Zelanda.
- En octubre de 2022, filtraron datos de estudiantes del LAUSD.

## ALPHV BlackCat

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2023/07/dark-web-profile-blackcat-ransomware-768x432.png"/>
</p>

- Es un grupo de ransomware conocido por ser el primero en usar el lenguaje de programación Rust.
- El grupo anunció su programa de afiliados RaaS (Ransomware-as-a-Service) en un foro de la dark web en diciembre de 2021.
- El grupo obtiene acceso inicial a sistemas objetivo mediante credenciales de usuario robadas o aprovechando vulnerabilidades conocidas en Microsoft Exchange.
- Una vez dentro, comprometen cuentas de usuario y administrador en AD para establecer objetos de directiva de grupo maliciosos (GPOs).
- Deshabilitan medidas de seguridad al eliminar software antivirus y obtienen cuentas de dominio utilizando herramientas como [AdFind](https://www.hackplayers.com/2015/05/analiza-la-informacion-de-tu-da-con-adfind.html) y [ADRecon](https://github.com/adrecon/ADRecon)
- Emplean la triple extorsión, donde además de robar datos sensibles antes de cifrar los archivos de la víctima y amenazar con su publicación (doble extorsión), amenazan con lanzar un ataque de denegación de servicio distribuido (DDoS) si no se cumplen sus demandas.

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2023/02/blackcat-infection-chain.jpg"/>
</p>

-  Implementar la autenticación multifactor (MFA) como requisito de acceso podría bloquear puntos de entrada comprometidos.
-  Mantener copias de seguridad fuera de línea es crucial al lidiar con ransomware.

## Lapsus$

- Grupo relativamente nuevo que ha llamado la atención mundial con ataques de alto perfil y métodos poco convencionales.
- Atacaron el Ministerio de Salud de Brasil, borrando 50 terabytes de datos.
- Luego apuntaron a empresas como CORREIOS, Claro, Impresa (Portugal), NVIDIA, Samsung, Ubisoft, Microsoft, y Okta.
- Exigió a NVIDIA eliminar la función LHR y liberar los controladores de GPU para Windows, Mac y Linux.
- Publicaron códigos fuente de Bing, Bing Map y Cortana de Microsoft en su canal de Telegram.
- Violación de Okta, ganando control total sobre las cuentas administrativas.
- TTPs:

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*tqGosO-G1oK_pgjc9Do9fA@2x.png"/>
</p>

- Lapsus$ no busca ocultar sus acciones, anuncia ataques en redes sociales y busca publicar filtraciones.
- Las defensas sólidas, MFA basado en token y protocolos de respuesta a incidentes son vitales.

## Tropical Scorpius

- Cuba es un ransomware basado en C++, utilizado por el grupo Cuba Ransomware en ataques de doble extorsión.
- Utilizan Cuba junto a un sitio de filtración de datos que publica información extraída de sistemas comprometidos.
- Apareció por primera vez a fines de 2019 afectando varias máquinas.
- Aunque se hace alusión a Cuba en imágenes y el nombre del grupo es Cuba, se presume una asociación con Rusia debido al uso del idioma ruso en el sitio de filtración de datos y durante negociaciones.
- El 4 de febrero, el ransomware afectó los Servicios de Transferencia Automática de Fondos (AFTS) en Seattle.
- El FBI informó que en diciembre de 2021, el grupo comprometió al menos 49 entidades en cinco sectores críticos, incluyendo finanzas, gobierno, salud, manufactura y tecnología.

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2022/03/stages-of-a-cuba-ransomware-attack--1024x512.png"/>
</p>

- Cuba Ransomware se asocia con Hancitor downloader para acceder a redes comprometidas.
- Utilizan Cobalt Strike para ejecutar scripts, realizar escaladas de privilegios y explorar redes comprometidas.
- Emplean herramientas como Netping y Protoping para escanear y recopilar información de la red.
- Utilizan acceso remoto y backdoors como Ficker Stealer o SystemBC para moverse lateralmente en la red.
  
## Cozy Bear

- Se asocia con agencias de inteligencia rusas, específicamente identificado como APT29.
- Poseen capacidades avanzadas para llevar a cabo ataques altamente dirigidos, como el ataque a la cadena de suministro de SolarWinds.
- Presumiblemente dirigido por el Servicio de Inteligencia Exterior de Rusia (SVR).
- Infiltraron la red del Comité Nacional Demócrata en 2015, causando una violación de datos detectada en 2016.
- Están detrás de operaciones como Operation Ghost, afectando al Ministerio de Asuntos Exteriores de algunos países europeos.
- Se les vincula con el malware WellMess utilizado en ataques a institutos de investigación de vacunas contra COVID-19.
- Utilizan plataformas de redes sociales y servicios en línea para comunicarse durante sus actividades maliciosas.
- Se valen de aplicaciones como Notion y sistemas como LegisWrite y eTrustEx para atacar a organizaciones estatales en la Unión Europea.
- Recientemente han empleado chats de Microsoft Teams para realizar ataques de ingeniería social.
- Aprovecharon una vulnerabilidad de WinRAR en ataques a embajadas europeas.
- También explotan vulnerabilidades críticas como [CVE-2018-13379](https://nvd.nist.gov/vuln/detail/CVE-2018-1337) de Fortinet FortiOS y otras.

## APT40

- Grupo patrocinado por China
- Desde al menos 2013, este actor ha apoyado los esfuerzos de modernización naval de China.
- También se ha observado un enfoque en países estratégicamente importantes para la Iniciativa del Cinturón y Ruta de la Seda
- APT40 utiliza una variedad de técnicas para el compromiso inicial, como explotación de servidores web, campañas de phishing y compromisos estratégicos en la web.
- Ciclo de vida del ataque:

<p align="center">
  <img src="https://ics-cert.kaspersky.com/wp-content/uploads/sites/6/2020/04/3-2.png"/>
</p>

- Utilizan malware como AIRBREAK, FRESHAIR y BEACON para penetrar los sistemas.
- Utilizan backdoors y herramientas como web shells para mantener el control en el entorno comprometido.
- Implica recopilar y transferir información, usando herramientas como rar.exe para comprimir y cifrar datos antes de la exfiltración.

## Earth Preta

- En noviembre de 2022, se reveló una gran campaña de phishing iniciada por Earth Preta, también conocido como Mustang Panda.
- La campaña apuntó a varios países de la región de Asia-Pacífico (APAC) a través de correos electrónicos de spear-phishing.
- Se identificó a entidades gubernamentales como uno de los principales objetivos del grupo.
- Desde principios de 2023, se observaron nuevos vectores de ataque utilizados por el grupo, como MIROGO y QMAGENT.
- Se descubrió un nuevo dropper llamado TONEDROP que libera el malware TONEINS y TONESHELL en diferentes regiones.
- Los documentos señuelo están escritos en birmano y contienen temas controvertidos entre países.
- Utilizan correos electrónicos de spear-phishing con enlaces de Google Drive para distribuir archivos maliciosos.
  

## Inteligencia de amenazas<a name="id9"></a>

## Threat Intelligence

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

## Attack Frameworks and Indicator Management

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


## Red Team<a name="id10"></a>

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

- Es una herramienta de código abierto que se utiliza para extraer credenciales de seguridad, como contraseñas, hashes de contraseñas, tokens de autenticación y claves de sesión, de sistemas operativos Windows.
- Mimikatz se puede utilizar para robar contraseñas de usuarios desprevenidos.
- Mimikatz se puede utilizar para adivinar contraseñas de usuarios.
- Mimikatz se puede utilizar para obtener privilegios elevados en un sistema operativo Windows.
- Puede incluir la identificación de credenciales débiles o desactualizadas, o la detección de vulnerabilidades en los protocolos de autenticación.
- Puede extraer contraseñas, hashes de contraseñas, tokens de autenticación y claves de sesión de una variedad de fuentes tales como:  memoria del sistema operativo, archivos de contraseñas, registros del sistema.
- Mimikatz puede generar tráfico de red que puede ser detectado por un firewall o un sistema de detección de intrusiones.
- puede registrar eventos en los registros del sistema que pueden ser detectados por un sistema de administración de eventos de seguridad.

```
# Extraer todas las contraseñas del almacén de credenciales del sistema operativo
mimikatz "sekurlsa::logonpasswords"

# Extraer el hash de contraseña de la cuenta de administrador
mimikatz "sekurlsa::logonpasswords /logonid:S-1-5-21-0-0-0"

# Extraer el token de autenticación de la cuenta de administrador
mimikatz "sekurlsa::logonpasswords /logonid:S-1-5-21-0-0-0 /ticket"

# Extraer la clave de sesión de la cuenta de administrador
mimikatz "sekurlsa::logonpasswords /logonid:S-1-5-21-0-0-0 /session"
```
 
## Malicious use of Registry

- El registro de Windows es una base de datos jerárquica que contiene información sobre la configuración del sistema operativo y los programas instalados.
- Los atacantes pueden abusar del registro para controlar el sistema operativo, ocultar malware o evadir la detección.
- Una de las técnicas que utilizan los analistas de malware para identificar el uso malicioso del registro es examinar los cambios que ha realizado el malware en el registro.
- Estos cambios pueden incluir la adición o eliminación de claves de registro, la modificación de valores de registro o la creación de nuevos servicios.
- El malware puede utilizar el registro para cambiar la configuración del sistema operativo, como la configuración de seguridad, la configuración de red o la configuración de inicio.
- El malware puede crear claves de registro que oculten la ubicación del malware o que hagan que el malware aparezca como un proceso legítimo.
- El malware puede crear registros de eventos falsos o modificar registros de eventos existentes para ocultar su actividad.
- Los atacantes pueden utilizar los servicios para ejecutar malware de forma persistente en el sistema operativo.
- Una vez creado el archivo de servicio, el atacante debe registrar el servicio en el registro.
- El atacante debe agregar una nueva clave de registro al subárbol `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services`.
- El malware fileless es un tipo de malware que no se almacena como un archivo independiente sino en en el registro o en la memoria del sistema.
- El malware fileless es más difícil de detectar que el malware tradicional porque no deja rastros en el disco duro.
- El Editor del Registro es una herramienta que se utiliza para modificar el registro de Windows.
 

## Blue Team<a name="id11"></a>

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


## Agradecimientos<a name="id12"></a>

- [MinTIC](https://www.mintic.gov.co/portal/inicio/)
- [BIOS](https://bios.co/)
- [CiberHub](https://www.ciberhub.co/formacion/)
- [Cyberbit](https://www.cyberbit.com/)
