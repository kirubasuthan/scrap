# scrap
To Share notes

kubectl create deployment hello-node1 --image=k8s.gcr.io/echoserver:1.4

 
kubectl expose deployment hello-node1 --type=LoadBalancer --port=8080

kubectl get pod
