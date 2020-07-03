pipeline {
    agent {
        kubernetes {
            yaml '''
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: busybox
    image: busybox
    command:
    - sleep
    args:
    - infinity
'''
            defaultContainer 'busybox'
        }
    }
    stages {
        stage('sample') {
            steps {
                sh 'echo hello from sample-app-1'
            }
        }
    }
}
