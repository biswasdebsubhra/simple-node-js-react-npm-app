pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000' 
        }
    }
    environment {
        CI = 'true'
        HOME = '.'
    }
    stages {
        stage('Build') {
            steps {
                sh 'id'
                sh 'ls -lrt'
		sh 'npm i sw-precache'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
