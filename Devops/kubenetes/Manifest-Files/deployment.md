# Topic: Deployment
---

**Kubernetes Deployment** is an object that helps you **run and manage your application automatically**.

It:

* Runs **multiple copies (replicas)** of your app
* **Restarts pods** if they crash (self-healing)
* **Scales up/down** easily
* Updates the app **without downtime** (rolling updates)


```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: deployement
spec:
  replicas: 3
  selector:
    matchLabels:
        app: gaming
  template:
    metadata:
      name: tmp-01
      labels:
         app: gaming
    spec:
      containers:
         - name: super-mario
           image: abhipraydh96/super-mario
           ports:
             - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
  name: svc-gaming
spec:
 selector:
    app: gaming
 ports:
   - port: 80
     targetPort: 80
     protocol: "TCP"
 type: NodePort
 ```

#### Commands:
````
kubectl get deploy
````
````
kubectl get svc
````
