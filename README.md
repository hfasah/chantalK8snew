# chantalK8snew

kubectl -n test  create deployment  app_1 --image redis  --replicas 5 --dry-run=client -o yaml > redis.yaml

kubectl create -f redis.yaml 
kubectl get deplyment -n test
kubectl get deployment -n test
vim autoscale.yaml
kubectl create -f autoscale.yaml
vim autoscale.yaml
kubectl create -f autoscale.yaml
kubectl get hpa -n test
kubectl get deployment -n test
vim autoscale.yaml
vim redis.yaml 
