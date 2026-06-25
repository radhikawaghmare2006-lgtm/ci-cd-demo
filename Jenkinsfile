pipeline {
    agent any

    tools {
        go 'test-jenkin'
    }

    environment {
        GO111MODULE = 'on'
    }

    stages {
        stage('Test') {
            steps {
                git 'https://github.com/radhikawaghmare2006-lgtm/ci-cd-demo.git'
                sh 'go test ./...'
            }
        }

        stage('Build') {
            steps {
                git 'https://github.com/radhikawaghmare2006-lgtm/ci-cd-demo.git'
                sh 'go build .'
            }
        }

        stage('Run') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/jk-jobs&& go-webapp-sample &'
            }
        }
    }
}
