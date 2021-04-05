pipeline {
    agent any

    stages {
        stage('Code') {
            steps {
                git 'https://github.com/Rajaram7/Maven-Demo.git'
            }
        }
        stage('Build') {
            steps {
                sh '''mvn clean'''
                sh '''mvn install'''
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp -rp "/var/lib/jenkins/workspace/demo-pipeline/multi-module/webapp/target/webapp.war"  "/opt/apache-tomcat/webapps"'
            }
        }
    }
}

