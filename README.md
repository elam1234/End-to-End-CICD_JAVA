" AUTOMATE SOFTWARE DEVELOPMENT AND DEPLOYMENT USING CICD  "

CICD IMPLEMENTATION FOR JAVA SPRING-BOOT-APP

INTRODUCTION :
Hello everyone, I Elamparithi M, am a DevOps Engineer, I am very passionate about contributing innovative projects in Cloud and DevOps cultures. In this document, I will describe a project where I automated software development and deployment using modern CI/CD practices. This project involved running the application manually, containerizing it with Docker, and implementing CI/CD pipelines using Jenkins for continuous integration and ArgoCD for continuous delivery on a Minikube cluster. 
 
PROJECT EXPLANATION :
developers who develop the software, while as a DevOps engineer make sure to automate the software development through DevOps practices such as a ci-cd this is a modern-day approach,  let me explain what I did in this project.
I began by running the application manually and creating a Dockerfile for containerization. Moving to CI/CD, I used Jenkins for continuous integration and ArgoCD for continuous delivery using GitOps principles.
In Jenkins, Docker was chosen as the agent machine for CI stages: cloning from GitHub, Maven packaging, SonarQube analysis, Docker image building, and Kubernetes YAML file updates via a shell script. It was so smooth that even Docker couldn't containerize my excitement!
ArgoCD on Minikube ensured Kubernetes deployment state consistency from Git repositories. It was like having a magic wand that made Kubernetes YAML files dance to the right tune!
This implementation reflects a modern DevOps approach, promoting efficient software development and deployment practices.

PROJECT HIGH-LEVEL STEPS :
EC2 Instance Setup:
Create an EC2 instance of t2.large size.
Install Jenkins, SonarQube, and Docker on the EC2 instance.
      2. Jenkins Configuration:
Install necessary plugins in Jenkins: Git, Maven, SonarScanner, and Docker Pipeline.
Store credentials securely in Jenkins for Docker Hub, Git, and SonarQube.

     3. Jenkins Pipeline (Jenkinsfile):
Write a Jenkinsfile with stages:
Setup Docker agent.
Clone the repository from GitHub.
Build source code using Maven.
Perform static code analysis with SonarQube.
Build and push Docker images to Docker Hub.
Update Kubernetes YAML files.
     4 .  Minikube Cluster and ArgoCD Setup:
Set up a Minikube cluster for Kubernetes orchestration.
Install and configure ArgoCD for continuous delivery.
      5.  GitHub Integration:
Configure a GitHub repository to store Kubernetes YAML manifests.
Create an application setup in ArgoCD for deploying applications from GitHub
     6. GitHub Webhook Configuration:
     Configure a GitHub webhook for triggering CI/CD pipelines 
automatically.

CHALLENGES FACED :
During this project, I encountered several challenges:
Running SonarQube on the root user, which did not start the SonarQube server. I created a new user to start the SonarQube server successfully.
Ensuring that the Docker agent contains dependencies required for each pipeline stage.
Storing Docker credentials securely in a secret file in the Jenkins credentials store.
Selecting the correct branch to update the Kubernetes YAML files.
Dealing with application sync issues in ArgoCD.

GITHUB LINK :
[https://github.com/elam1234/End-to-End-CICD_JAVA.git]

CONCLUSION :
In automating software development and deployment using CI/CD, I navigated challenges and embraced modern DevOps practices. From manual runs and Docker containerization to a robust CI/CD pipeline with Jenkins and ArgoCD, this project exemplifies efficiency and reliability in software delivery. Check out the GitHub repository [https://github.com/elam1234/End-to-End-CICD_JAVA.git] for detailed insights into this journey.


          


