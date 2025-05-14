#  Deploy to EC2 server from Jenkins Pipeline

## **Project Overview**
This project is divided into 3 part. 
   - Deploy WebApp Container via Jenkins Pipeline on EC2
   - Deploy Java Maven App via Jenkins Pipeline on EC2 Instance
   - Deploy Java Maven App via Jenkins Pipeline on EC2 Instance using Docker-Compose File
---

## **Features**

### **Jenkins Pipeline to deploy on AWS EC2**

- Deploy Java Maven App via Jenkins Pipeline on EC2 Instance**

   - Installed SSH agent plugin on Jenkins.
   - Created ssh credentials type for EC2 on Jenkins.
   - Configured Jenkinsfile to use the sshAgent and execute docker run command on EC2.
   - Docker Login to DockerHub or your other private Docker Repository (if you haven’t already).
   - Security Group configured: Added Jenkins IP Address and opened port to access Web App from Browser.
   - Deploy Webapp on EC2 Instance by executed Multi-Branch Pipeline.
   - Access Application on port 3080 in the browser

- Deploy Java Maven App via Jenkins Pipeline on EC2 Instance**
   - Configured Jenkinsfile to build and deploy on EC2 Instance
   - Executed Multi-Branch Pipeline on Jenkins
   - Try to deploy an App with docker-compose and run a shell script


### **Deploy using Docker Compose (Docker-Compose, ECR)**
- Deploy Java Maven App via Jenkins Pipeline on EC2 Instance using Docker-Compose File
   - Installed Docker-Compose on EC2 Instance
   - Created docker-compose.yaml file
   - Configured Jenkinsfile to execute docker-compose command
   - Executed Jenkins Pipeline and deploy to AWS EC2 Instance
   - Improvement: Extract to Shell Script

### **Complete Pipeline (Docker-Compose, ECR, Dynamic versioning)**
- as before with dynamic versioning
   - Adjusted Jenkinsfile to include dynamic versioning
   - Executed Jenkins Pipeline and deploy to AWS EC2 Instance

### **Jenkins Pipeline to deploy on AWS EC2**

- Deploy Java Maven App via Jenkins Pipeline on EC2 Instance**

   - Installed SSH agent plugin on Jenkins.
   - Created ssh credentials type for EC2 on Jenkins.
   - Configured Jenkinsfile to use the sshAgent and execute docker run command on EC2.

     ![image](https://github.com/user-attachments/assets/c639ce5a-6e9c-4c2f-9e4a-76228563ef6c)

   - Docker Login to DockerHub or your other private Docker Repository (if you haven’t already).
   - Security Group configured: Added Jenkins IP Address and opened port to access Web App from Browser.
   - Deploy Webapp on EC2 Instance by executed Multi-Branch Pipeline.
 
     ![image](https://github.com/user-attachments/assets/46f064ec-760d-4eea-817f-66b46900dda2)


     ![image](https://github.com/user-attachments/assets/babb6882-08b2-49c8-9243-7360017ee51b)

   - Access Application on port 3080 in the browser

     ![image](https://github.com/user-attachments/assets/76ee8b29-d498-4750-ab91-f02e4c382922)


- Deploy Java Maven App via Jenkins Pipeline on EC2 Instance**
   - Configured Jenkinsfile to build and deploy on EC2 Instance
   - Executed Multi-Branch Pipeline on Jenkins
   - Try to deploy an App with docker-compose and run a shell script


### **Deploy using Docker Compose (Docker-Compose, ECR)**
- Deploy Java Maven App via Jenkins Pipeline on EC2 Instance using Docker-Compose File
   - Installed Docker-Compose on EC2 Instance
 
     ![image](https://github.com/user-attachments/assets/05f520db-3b7d-4877-a1a7-aaf38961e222)

   - Created docker-compose.yaml file
   - Configured Jenkinsfile to execute docker-compose command
     
     ![image](https://github.com/user-attachments/assets/5d22a633-eda8-4c4b-96b6-36b7dcb7056e)

   - Executed Jenkins Pipeline and deploy to AWS EC2 Instance
   - Improvement: Extract to Shell Script

     ![image](https://github.com/user-attachments/assets/667259f8-348e-4d07-8c1c-2a9d3f155f4e)

     ![image](https://github.com/user-attachments/assets/dffb4a29-f99a-4e8e-97d6-871d67cac4a3)



### **Complete Pipeline (Docker-Compose, ECR, Dynamic versioning)**
- as before with dynamic versioning
   - Adjusted Jenkinsfile to include dynamic versioning
   - Executed Jenkins Pipeline and deploy to AWS EC2 Instance

     ![image](https://github.com/user-attachments/assets/9b90519f-453b-4776-b7c0-1756868e3676)



