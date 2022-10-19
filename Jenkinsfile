// Jenkinsfile for testing purposes
pipeline {
  agent {
    kubernetes {
      cloud "kubernetes"
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
        podTemplate(cloud: 'kubernetes', containers: [containerTemplate(args: '9999999', command: 'sleep', image: 'busybox', name: 'busybox')], label: 'template1', name: 'template1', namespace: 'devops') {
          node("template1") {
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
}
