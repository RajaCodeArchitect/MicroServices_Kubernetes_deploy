# deploying microservices on Kubernetes

## installed kubctl and minikube in local machine
- created group using `sudo usermod -aG docker $USER && newgrp docker`
  
 ## create & run pods and services
 - `kubectl create -f voting-app-pod.yaml`
 - `kubectl create 0f voting-app-service.yaml`
  - added `alias k-kubernetes` in local machine
  - `kubctl get pods,svc`
  - if you not sure about the IP of service you can run the command
  - `minikube service <nameOtheService> --url`
  - example: `minikube service voting-service --url`
  - `http://192.168.49.2:30004`
  - ![Alt text](assets/image-1.png)
  - `k create -f redis-pod.yaml`
  - `k create -f redis-service.yaml`
  - `minikube service voting-service --url` it will url
  - `minikube start ` if it's stop before running kubectl make sure to check minikube status
  - `kubectl get pods,svc,deployment`
  - `kubectl create -f voting-app-deploy`
  - `kubectl create -f voting-app-service`
  - `kubectl delete service <name>`
  - `kubectl scale deployment voting-app-deploy --replicas=6`


![Alt text](assets/image.png)