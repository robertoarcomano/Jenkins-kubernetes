pipeline {
    agent none
    stages {
        stage('Test') {
            agent {
                kubernetes {
                    cloud "kubernetes"
                    podTemplate(cloud: 'kubernetes', inheritFrom: 'kubectl', label: 'kubectl', name: 'kubectl', namespace: 'devops') {
                        stages {
                            stage("test") {
                                steps {
                                    sh "hostname"
                                }
                            }
                        }
                    }
                }
            }
        }
    }
}