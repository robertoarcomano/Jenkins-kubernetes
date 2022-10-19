// Jenkinsfile for testing purposes
pipeline {
  agent {
    kubernetes {
      cloud "kubernetes"
      yamlFile 'pod.yaml'
      yamlFile 'pod1.yaml'
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
        container("container1") {
          script {
            echo 'container1: '
            sh 'hostname'
            sh 'cat /etc/issue'
          }
        }
        container("container2") {
          script {
            echo 'container2: '
            sh 'hostname'
            sh 'cat /etc/issue'
          }
        }
        container("container3) {
          script {
            echo 'container3: '
            sh 'hostname'
            sh 'cat /etc/issue'
          }
        }
        container("container4") {
          script {
            echo 'container4: '
            sh 'hostname'
            sh 'cat /etc/issue'
          }
        }
      }
    }
  }
}
