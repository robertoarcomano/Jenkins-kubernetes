pipeline {
    agent {
        kubernetes {
            cloud "kubernetes"
            yamlFile 'pod.yaml'
        }
    }
    stages {
        stage("First") {
            steps {
                container("bootvar-container") {
                    sh "kubectl"
                }
            }
        }
    }
}