# Kubernetes-nodejs-app
Sample Nodejs application deployed with [Kubernetes](https://kubernetes.io)

## Deployment

 - Create deployment
 - `kubectl apply -f node-deploy.yaml`
 - Expose service by creating a service yaml file as
 - `node-service.yaml`
 - Get mapped port for the app
 - `kubectl get service`
 - Visit k8s cluster provider domain in the browser `http://b2659cf2-c5f9-404a-98a5-c789a9adf67b.k8s.civo.com/nodes/docs/` in my case.

## Services

 - Create services 
 - `kubectl apply -f node-service.yaml`
 - Get mapped port for the app
 - `kubectl get service`

## Secret

 - Create secret for credentials in nodejs app 
 - `kubectl create secret generic wondersecret --from-literal=nodesecret5=`

## Ingress

 - Create ingress
 - `kubectl apply -f node-ingress.yaml`
 - Use a loadbalancer for ingress
 - In this project, I have used `traefik` 
 - Set host to a kubernetes service provider 
 - In this project, I have used `civo` 

