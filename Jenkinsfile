#!/usr/bin/env groovy

pipeline {
    agent any
    stages {   
        stage('deploy') {
          environment {
              AWS_ACCESS_KEY_ID = credentials('jenkins_aws_access_key_id') 
              AWS_SECRET_ACCESS_KEY = credentials('jenkins_aws_secret_access_key')
          }
            steps {
                script{
                    echo "deploying docker image"
                    sh "kubectl create deployment nginx-deployment --image=nginx"
                }
            }
        }
    }
}
