# Scrap
To Share notes

## Create Minikube deployment
`kubectl create deployment hello-world --image=k8s.gcr.io/echoserver:1.4` 

## Create service 
`kubectl expose deployment hello-world --type=NodePort --port=8080`

## Enable port forwarding and view the web service in http://localhost:7000

`kubectl port-forward services/hello-world 7000:8080 &`

## Delete the deployment
`kubectl delete service hello-world ` </BR>
 kubectl delete deployment hello-world `

## Get details 
`
kubectl get pod </BR>
kubectl get services </BR>
kubectl get deployment </BR>
`

## Bring up Tomcat 

`kubectl apply -f deployment.yaml ` </BR>
`kubectl expose deployment tomcat-deployment --type=NodePort ` </BR>
`minikube service tomcat-deployment --url`</BR>

`kubectl describe pod <pod-name>`

#kubectl expose deployment hello-node1 --type=LoadBalancer --port=8080

# Scaling app
`kubectl scale --replicas=4 deployment/tomcat-deployment`

`kubectl expose deployment tomcat-deployment --type=LoadBalancer --port=8080 --target-port=8080 --name tomcat-load-balancer`

# Simple http server spitting env
`kubectl create deployment httpend --image=bretfisher/httpenv ` </BR>
`kubectl scale deployment/httpend --replicas=4 ` </BR>
`kubectl expose deployment httpend --port=8888 `</BR>
 
Create nodeport service</BR>
`kubectl expose deployment httpend --port=8888 --name=httpend-np --type=NodePort `
