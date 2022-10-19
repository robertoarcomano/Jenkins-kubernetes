// Jenkinsfile for testing purposes
pipeline {
  agent {
    kubernetes {
      cloud "kubernetes"
      yamlFile 'pod-ubuntu.yaml'
    }
  }
  environment {
    EMAIL_RECIPIENT="info@robertoarcomano.com"
    EMAIL_TEST_SUBJECT="Test Masterit: "
    EMAIL_BUILD_SUBJECT="Build Masterit: "
    TEST_STATUS="FAILED"
    BUILD_STATUS="FAILED"
    EMAIL_SENDER="Jenkins - Oracle3 <info@robertoarcomano.com>"
    OUTPUT=""
    VERSION=""
  }
  stages {
    stage('check1') {
      steps {
        container("ubuntu") {
          script {
            sh 'hostname'
            sh 'sleep 10'
            sh 'cat /etc/issue'
          }
        }
      }
    }
  }
}
