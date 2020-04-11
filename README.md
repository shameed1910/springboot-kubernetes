# springboot-kubernetes

# Create a docker image by using the below command

docker build -t springboot-k8s:1.0

# Create a deployment by using the below command

kubectl run springboot-k8s --image=springboot-k8s:1.0 --port 8080 --image-pull-policy=Never

# Created a service by using the below command

kubectl expose deployment springboot-k8s --type=NodePort

# You can scale the deployment by using the below command

kubectl scale --replicas=3 deployment/springboot-k8s

# You can autoscale the deployment by using the below command

kubectl autoscale deployment springboot-k8s --cpu-percent=50 --min=1 --max=10

# Create a docker image 2.0 version to update the deployment by using the below command

docker build -t springboot-k8s:2.0

# You can update the deployment by using the below command

kubectl set image deployment springboot-k8s springboot-k8s=springboot-k8s:2.0

# Command to see a list of Pods

kubectl get pods

# Command to see a list of Deployments

kubectl get deployments

# Command to see a list of Services

kubectl get services

# Get details of your deployments

kubectl get describe deployments

# Get details of your replicas

kubectl get describe deployments

# Command to create a deployment object by using the yml file

kubectl apply -f deployment.yml

# Command to create a service object by using the yml file

kubectl apply -f service.yml





