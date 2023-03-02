pipeline {
    agent none
    stages {
        stage('Test') {
            agent {
                kubernetes {
                    cloud "kubernetes"
                    podTemplate(cloud: 'kubernetes') {
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