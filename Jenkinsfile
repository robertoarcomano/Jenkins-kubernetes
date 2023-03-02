pipeline {
  agent {
    kubernetes {
      cloud 'kubernetes'
      label 'mypod'
      containerTemplate {
        name 'maven'
        image 'bitnami/kubectl'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
    stage('Run maven') {
      steps {
        sh 'kubectl --help'
      }
    }
  }
}