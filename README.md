# Microservices Docker Kubernetes

### Kubernetes Vocab
- Node
  - Kubelet
  - Communicates with master
  - Runs pods
- Pod
  - Runs 1+ containers
  - Exists on a node
- Service
  - Handles requests
  - Usually a load balancer
- Deployment
  - Defines desired state - kubernetes handles the rest

### K8 Commands
```bash
  minikube start
  
  minikube stop
  
  minikube status
  
  minikube dashboard
```
#### Start
```bash
  kubectl get pods
  
  kubectl get deployments
```
#### Create/Delete
```bash
  kubectl create -f deployment.yml
  
  kubectl delete -f=deployment.yml
  
  kubectl apply -f deployment.yml
```
#### Docker
```bash
  docker build -t andriizilnyk/exampleapp:v1.0.0 .
  
  docker run -p 8080:8080 -d andriizilnyk/exampleapp:v1.0.0
```
#### In order to push image into `https://hub.docker.com/` you need to login
```bash
  docker login
  
  docker push andriizilnyk/exampleapp:v1.0.0
```
#### Test if app is running
```bash
  minikube ip
```
- Output
```bash
  192.168.49.2:30003
```