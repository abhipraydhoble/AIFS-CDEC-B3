# StatefulSet
A StatefulSet runs a group of Pods, and maintains a sticky identity for each of those Pods. 
This is useful for managing applications that need persistent storage or a stable, unique network identity.

StatefulSets are valuable for applications that require one or more of the following:

Stable, unique network identifiers.
Stable, persistent storage.
Ordered, graceful deployment and scaling.
Ordered, automated rolling updates.

#### Example 1:
```yaml
apiVersion: apps/v1
kind: StatefulSet
metadata:
  name: redis
spec:
  serviceName: "redis"
  replicas: 3
  selector:
    matchLabels:
      app: redis
  template:
    metadata:
      labels:
        app: redis
    spec:
      containers:
      - name: redis
        image: redis:5.0.5
        ports:
        - containerPort: 6379
          name: redis
  volumeClaimTemplates:
  - metadata:
      name: redis-data
    spec:
      accessModes: [ "ReadWriteOnce" ]
      resources:
        requests:
          storage: 1Gi
```

````
kubectl get sts
````
````
kubectl get pods
````
#### Example 2:
````
apiVersion: apps/v1
kind: StatefulSet
metadata:
  name: mariadb
spec:
  serviceName: "mariadb"
  replicas: 3
  selector:
    matchLabels:
      app: mariadb
  template:
    metadata:
      labels:
        app: mariadb
    spec:
      containers:
      - name: mariadb
        image: mariadb:10.6
        ports:
        - containerPort: 3306
          name: mariadb
  volumeClaimTemplates:
  - metadata:
      name: mariadb-data
    spec:
      accessModes: [ "ReadWriteOnce" ]
      resources:
        requests:
          storage: 1Gi
````

## DaemonSet
A DaemonSet ensures that all (or some) Nodes run a copy of a Pod.
Some typical uses of a DaemonSet are:
running a cluster storage daemon on every node
running a logs collection daemon on every node
running a node monitoring daemon on every node
```yaml
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: app1
spec:
  selector:
    matchLabels:
      app: app1
  template:
    metadata:
      labels:
        app: app1
    spec:
      containers:
        - name: app1-container
          image: nginx
          ports:
            - containerPort: 80
```

<img width="1233" height="568" alt="image" src="https://github.com/user-attachments/assets/3a166699-775d-49eb-af2c-52536769c74d" />
