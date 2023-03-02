pipeline {
    agent {
        kubernetes {
            cloud "kubernetes"
            podTemplate {
                node("kubectl") {
                    stage('Run shell') {
                        sh 'echo hello world'
                    }
                }
            }
        }
    }
    stages {
    }
}