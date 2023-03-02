pipeline {
    agent {
        kubernetes {
            cloud "kubernetes"
            label "build-pod"
            yamlFile 'pod.yaml'
        }
    }
    stages {
        stage("First") {
            steps {
                container("bootvar-container") {
                    sh "ls -lart"
                }
            }
        }
    }
}