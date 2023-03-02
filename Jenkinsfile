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
                    sh "apt update"
                    sh "apt install -y wget"
                    sh "wget https://dl.k8s.io/v1.26.2/bin/linux/arm64/kubectl"
                    sh "chmod 755 kubectl"
                    sh "./kubectl"
                }
            }
        }
    }
}