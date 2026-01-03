## create new file
````
vim deployment.yaml
````

````
apiVersion: apps/v1
kind: Deployment
metdata:
  name: netflix
spec:
  replicas: 3
  selector:
   matchLabels:
    app: netflix 
  template: 
    metadata:
     labels: 
       app: netflix
    spec:
      containers:
        - name: c1 
          image: abhipraydh96/streaming 
---
apiVersion: v1
kind: Service 
metdata: 
  name: svc-netflix 
spec:
 selector: 
    app: netflix
 ports:
      - protocol: "TCP"
        port: 80
        targetPort: 80
 type: NodePort
````

## commands
````
kubectl apply -f deployment.yaml
````
````
kubectl get pods
````
````
kubectl get svc
````
nodeport: external access [30000-32767]
loadbalancer: externl access
````
