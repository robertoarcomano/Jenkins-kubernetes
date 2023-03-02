pipeline {
    agent {
        kubernetes {
            label 'kubectl'
            podTemplate {
                containerTemplate {
                    name 'dind-jdk8-maven3'
                    image 'eu.gcr.io/jenkins-demo/dind-jdk8-maven3:v4'
                    ttyEnabled true
                    command 'cat'
                }
            }
        }
    }
    stages {
        stage('Test') {
          steps {
            sh 'hostname'
          }
        }
    }
}
