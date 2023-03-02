pipeline {
    agent none
    stages {
        stage("1.k8s") {
            agent {
                kubernetes {
                    yaml podTemplate
                    defaultContainer 'k8s'
                }
            }
            steps {
                sh """
                    mvn -version
                """
            }
        }
        stage("2. k8s") {
            agent { label 'k8s' }
            steps {
                sh """
                    mvn -version
                """
            }
        }
        stage("win") {
            agent { label 'windows' }
            steps {
                bat "dir"
            }
        }
    }
}