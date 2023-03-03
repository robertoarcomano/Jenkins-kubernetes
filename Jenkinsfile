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
                container("kubectl") {
                    sh "cat"
                    sh "apt update"
                    sh "apt install -y wget"
                    sh "pwd"
                    sh "wget https://dl.k8s.io/v1.26.2/bin/linux/arm64/kubectl"
                    sh "ls -al"
                    sh "chmod 755 kubectl"
                    sh "./kubectl get pods"
                }
            }
        }
    }
}
