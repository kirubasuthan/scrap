# scrap
To Share notes

# Create Minikube deployment
kubectl create deployment hello-node1 --image=k8s.gcr.io/echoserver:1.4

# Create service 
kubectl expose deployment hello-node1 --type=NodePort --port=8080

# Enable port forwarding and view the web service in http://localhost:7000

kubectl port-forward services/hello-world 7000:8080

# Delete the deployment

kubectl get pod
kubectl get services
kubectl get deployment



#kubectl expose deployment hello-node1 --type=LoadBalancer --port=8080
