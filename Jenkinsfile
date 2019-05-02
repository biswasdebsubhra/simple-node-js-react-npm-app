pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh '/usr/bin/sudo npm install'
            }
        }
        stage('Test') {
            steps {
                sh '/usr/bin/sudo ./jenkins/scripts/test.sh'
            }
        }
    }
}
