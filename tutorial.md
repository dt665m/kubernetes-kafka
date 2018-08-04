## Brand New Cluster
```
#enable rbac
kubectl create clusterrolebinding cluster-admin-binding --clusterrole cluster-admin --user [USER EMAIL]

kubectl apply -f ./00-namespace.yml
kubectl apply -f ./rbac-namespace-default
kubectl apply -f ./configure/gke-storageclass-broker-pd.yml
kubectl apply -f ./configure/gke-storageclass-zookeeper-ssd.yml
kubectl apply -f ./zookeeper
kubectl apply -f ./kafka
kubectl apply -f ./outside-services
```