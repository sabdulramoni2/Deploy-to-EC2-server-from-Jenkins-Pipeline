#  Deploy to EC2 server from Jenkins Pipeline

## **Project Overview**
This project is divided into 3 part. 
   - Deploy WebApp Container via Jenkins Pipeline on EC2
   - Deploy Java Maven App via Jenkins Pipeline on EC2 Instance
   - Deploy Java Maven App via Jenkins Pipeline on EC2 Instance using Docker-Compose File
---

## **Features**
- Installed Java on the server followed by Nexus on server, created a new Linux User for Nexus and changed the permissions of Nexus executable and the Sonatype-work folder.
- Set Nexus configuration to run as a Nexus user and started Nexus with the Nexus User.
- Configured Firewall rules to open port 8081 to access the Nexus server from the web browser.
- Created new user on Nexus with permission to upload artifacts.
- Build a jar file with Gradle and upload it to Nexus.
