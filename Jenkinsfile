#!/usr/bin/env groovy

library identifier: 'jenkins-shared-library@master', retriever: modernSCM(
    [$class: 'GitSCMSource',
    remote: 'https://gitlab.com/twn-devops-bootcamp/latest/09-aws/jenkins-shared-library.git',
    credentialsID: 'gitlab-credentials'
    ]
)

pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }

    environment {
        IMAGE_NAME = 'ashiwaju/jupiter12:java-maven-1.0'
    }
    stages { 
        
        stage('build app') {
            steps {
                echo 'building application jar...'
                buildJar()
            }
        }
        stage('build image') {
            steps {
                script {
                    echo 'building the docker image...'
                    buildImage(env.IMAGE_NAME)
                    dockerLogin()
                    dockerPush(env.IMAGE_NAME)
                }
            }
        } 
        stage("deploy") {
            steps {
                script {
                    echo 'deploying docker image to EC2.......'
                    def dockerComposeCmd = "docker-compose -f docker-compose.yaml up --deatch"
                    
                    sshagent(['ec2-server-key']) {
                        sh "scp docker-compose.yaml ec2-user@ip-172-31-36-44:/home/ec2-user"
                       sh "ssh -o StrictHostKeyChecking=no ec2-user@3.19.213.93 ${dockerCmd}"      
                    }
                }
            }
        } 
        
    }
}
