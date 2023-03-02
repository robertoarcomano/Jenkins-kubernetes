pipeline {
    agent {
        kubernetes {
            cloud "kubernetes"
            podTemplate(label: 'kubectl') {
                node('kubectl') {
                    sh 'Hello world!'
                }
            }
        }
    }
    stages {
    }
}