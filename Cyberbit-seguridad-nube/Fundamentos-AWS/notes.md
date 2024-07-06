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
