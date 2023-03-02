pipeline {
    agent {
        kubernetes {
            cloud "kubernetes"
            label "build-pod"
            yaml '''
apiVersion: v1
kind: Pod
metadata:
  namespace: devops
  labels:
    job: bootvar-build-pod
spec:
  containers:
  - name: bootvar-container
    image: alpine:latest
    tty: true
    command: ['cat']
'''
        }
    }
    stages {
        stage("First") {
            steps {
                container("bootvar-container") {
                    sh "ls -lart"
                }
            }
        }
    }
}