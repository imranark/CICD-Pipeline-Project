![image](https://user-images.githubusercontent.com/9801131/236262736-73e1257f-827c-4d9b-bd26-23a5ab3ff2fa.png)

<h1>kubernetes-configmap-reload</h1>
<h2>Pre-requisites:</h2>
- Install Git
- Install Maven
- Install Docker
- EKS Cluster

#Clone code from github:
 *git clone https://github.com/ganasai88/CI-CD-Project.git \n
 *cd CI-CD-Project

#Build Maven Artifact:

mvn clean install

# Build Docker image for Springboot Application
-docker build -t dockerhubuserid/imagename
-docker login

#Push docker image to dockerhub
*docker push dockerhubuserid/imagename

#Deploy Spring Application:
*kubectl apply -f .

#Check Deployments, Pods and Services:

*kubectl get deploy
*kubectl get pods
*kubectl get svc

Now Goto Loadbalancer and check whether service comes Inservice or not, If it comes Inservice copy DNS Name of Loadbalancer and Give in WebUI

#Now we can cleanup by using below commands:
*kubectl delete deploy kubernetes-configmap-reload
*kubectl delete svc kubernetes-configmap-reload
