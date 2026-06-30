pipeline {
    agent any

    tools {
        go 'gotest'
    }

    environment {
        GO111MODULE = 'on'
    }

    stages {
        stage('Test') {
            steps {
                git 'https://github.com/databinaries001/ci-cd-demo.git'
                sh 'go test ./...'
            }
        }
    }
}
