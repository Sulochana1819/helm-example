# helm-example

# cloneing the repository

git clone https://github.com/johnpapa/node-hello
 # step 2 : creating docker image and push to Dockerhub

 $ docker build -t sulochana19/node-hello-world .
 $ docker push sulochana19/node-hello-world:latest

 # step 3 installing helm and create helm charts
 
Install Helm if you haven't already: https://helm.sh/docs/intro/install

# Create Helm charts

$helm create node-hello-world

values.yaml: Define default values for your application.
templates/: Place Kubernetes manifests templates here. You'll have deployment, service, 

$helm helm package node-hello-world

$ helm install node-hello-world ./node-hello-world-0.1.0.tgz

# step 4 push the helm charts to Git repository

# step 5 install ArgoCD 

1. created namespace argocd
2. get the all pods (kubectl get pods -n argocd)

   $kubectl get pods -n argocd

   $ kubectl get services -n argocd

edited argocd-server service change the port to ClusterIP to NodePort

run the command 

$minikube service argocd -service -n argocd

# step 6 : Deploying ArgoCD application

Created argocd-application.yaml
                      
   




 
