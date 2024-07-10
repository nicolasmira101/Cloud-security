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
