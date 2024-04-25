# Voting-App
# Kubernetes Demo: Commands and Pod/Service Creation

## Kubernetes Commands

### Get Information

- **List all pods:**
  ```bash
  kubectl get pods

- **List all services:**
  ```bash
  kubectl get services

- **List all replicasets:**
  ```bash
  kubectl get replicasets

- **List pods and services together:**
  ```bash
  kubectl get pods,svc

- **List all deployments:**
  ```bash
  kubectl get deployments

- **Describe a specific resource (pod, service, deployment):**
  ```bash
  kubectl describe <resource> <name>

- **Delete a specific pod, service, or deployment:**
  ```bash
  kubectl delete <resource> <name>

- **Scale a deployment to a specific number of replicas:**
  ```bash
  kubectl scale deploy <name> --replicas=<number>

- **Get the URL of a service (Minikube):**
  ```bash
  minikube service <service-name> --url

## Create Pods and Services

- **Create voting app pod and service:**
  ```bash
  kubectl create -f voting-app-pod.yaml
  kubectl create -f voting-app-service.yaml

- **Create Redis pod and service:**
  ```bash
  kubectl create -f redis-pod.yaml
  kubectl create -f redis-service.yaml

- **Create Postgres pod and service:**
  ```bash
  kubectl create -f postgres-pod.yaml
  kubectl create -f postgres-service.yaml

- **Create result app pod and service:**
  ```bash
  kubectl create -f result-pod.yaml
  kubectl create -f result-service.yaml

- **Create worker pod:**
  ```bash
  kubectl create -f worker-pod.yaml

## Create Deployments
> [!NOTE]
> Note: If services are already terminated, they should be restarted before creating deployments. 

- **Create worker app deployment:**
  ```bash
  kubectl create -f worker-app-deploy.yaml

- **Create Postgres deployment:**
  ```bash
  kubectl create -f postgres-deploy.yaml

- **Create voting app deployment:**
  ```bash
  kubectl create -f voting-app-deploy.yaml

- **Create Redis deployment:**
  ```bash
  kubectl create -f redis-deploy.yaml

- **Create result app deployment:**
  ```bash
  kubectl create -f result-app-deploy.yaml

- **Resource Cleanup:**
  ```bash
  kubectl delete -f .