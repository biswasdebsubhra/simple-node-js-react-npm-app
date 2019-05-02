pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000' 
        }
    environment {
        HOME = '.'
    }
  }
/*    environment {
        CI = 'true'
    } */
    stages {
        stage('Build') {
            steps {
                sh 'id'
                sh 'ls -lrt'
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
