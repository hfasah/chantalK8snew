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



DevOps Take Home Exercise
Thank you for your interest in 7shifts. We appreciate your dedication for this take home
exercise, and for this reason we don’t expect you to spend more than 2 hours on this. If you
don’t finish that’s OK, you’ll have an opportunity to speak more about it during the interview.
Preamble
1. Assume you’re running on your favourite cloud (Azure, AWS, GCP) - you don’t have to
make this work specifically for GCP GKE.


2. Create a README.md that outlines your line of thinking for the solution


4. Create plain kubernetes resources (yaml or json). Please return this file in your response
with any other materials you want to share with us.
4. You can make the following assumptions
a. Each system you’re deploying has its own isolated database. You don’t have to
worry about the type. You can assume the database is in the same region as
your k8s
b. You can use any docker image you’d like for your containers. It’s just an
example, and does not have to work. Any, say, default php docker you can
deploy on a pod. What the container is does not matter - but we’ll be talking
about two different containers in the exercise, one for users, one for shifts.
c. Assume daily bell-curve scaling. High traffic during the day, low traffic during
night


Exercise
1. We want to deploy two containers that scale independently from one another
○ Container 1: This container runs code that runs a small API that returns users
from a database
○ Container 2: This container runs code that runs a small API that returns shifts
from a database.
2. For the best user experience auto scale this service when average CPU reaches 70%
3. Ensure the deployment can handle rolling deployments and rollbacks
4. Your development team should not be able to run certain commands on your k8s cluster,
but you want them to be able to deploy and roll back. What types of IAM controls do you
put in place?


Bonus
● How would you apply the configs to multiple environments (staging vs production)?
● How would you auto scale the deployment based on network latency instead of CPU?
