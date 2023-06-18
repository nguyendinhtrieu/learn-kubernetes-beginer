# Learn kubernetes for beginner

# 1. Prerequisite

- You need to install Docker: https://docs.docker.com/engine/install/

# 2. Install minikube

- Minikube is an open-source tool that allows you to run and manage Kubernetes clusters locally. It enables developers to set up a single-node Kubernetes cluster on their local machine for testing, development, and experimentation purposes. Minikube provides an easy and convenient way to learn, develop, and deploy applications on Kubernetes without the need for a full-scale production cluster. It is commonly used by developers to explore Kubernetes features, develop applications locally, and validate deployment configurations before moving to a production environment.
- Install minikube [here](https://minikube.sigs.k8s.io/docs/start/)
- Start minikube with docker driver

```
minikube start --driver docker
```

- Checking minikube status

```
minikube status
```

# 3. Install kubectl

- kubectl is a command-line tool used for interacting with Kubernetes clusters. It allows you to manage and control Kubernetes resources, such as deploying and scaling applications, inspecting cluster state, viewing logs, and executing commands inside containers running in the cluster. With kubectl, you can perform various operations and manage your Kubernetes infrastructure from the command line.
- Install kubectl [here](https://kubernetes.io/docs/tasks/tools/)
- Get status of node

```
kubectl get node
```

# 4. Running applications

- **Apply manages application through files defining K8s resources**

```
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml
```

- **Get all components in cluster**

```
kubectl get all
```

- **Get config map & secret**

```
kubectl get configmap
kubectl get secret
```

- **See more detail about the certain component**

```
kubectl describe service webapp-service
kubectl describe pod webapp-deployment-6897cdc4c7-6l49c
```

- **Checking log**

```
kubectl logs webapp-deployment-6897cdc4c7-6l49c
```

- **Get services**

```
kubectl get svc
```

- **Get ip of minikube**

```
minikube ip
kubectl get node -o wide # wide output
```

# 5. Reference

- https://www.youtube.com/watch?v=s_o8dwzRlu4
