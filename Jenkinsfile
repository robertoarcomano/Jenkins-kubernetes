// Jenkinsfile for testing purposes
pipeline {
  agent {
    kubernetes {
      cloud "kubernetes"
      yaml '''
        apiVersion: v1
        kind: Pod
        metadata:
          labels:
            some-label: some-label-value
          namespace: devops
        spec:
          containers:
          - name: ubuntu
            image: ubuntu
            command:
            - cat
            tty: true
        '''
      yaml '''
        apiVersion: v1
        kind: Pod
        metadata:
          labels:
            some-label: some-label-value
          namespace: devops
        spec:
          containers:
          - name: busybox
            image: busybox
            command:
            - cat
            tty: true
        '''
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
    stage('ubuntu') {
      steps {
        container("ubuntu") {
          script {
            sh 'hostname'
            sh 'cat /etc/issue'
          }
        }
      }
    }
    stage('busybox') {
      steps {
        container("busybox") {
          script {
            sh 'hostname'
            sh 'cat /etc/issue'
          }
        }
      }
    }
  }
}
