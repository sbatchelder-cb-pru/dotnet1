pipeline {
    agent {
        kubernetes {
          yaml"""
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: dotnet6
    image: mcr.microsoft.com/dotnet/sdk:6.0
    tty: true
"""
        }
    }

    stages {
        stage('Example Build') {
            steps {
                bat "dotnet -help"
            }
        }
    }
}
