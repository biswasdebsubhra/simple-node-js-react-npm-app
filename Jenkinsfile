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
<<<<<<< HEAD
                sh 'npm install --unsafe-perm=true --allow-root'
=======
                sh '/usr/bin/sudo npm install'
>>>>>>> fe38dbff253b81e0dca20f9d326410bdec6138ed
            }
        }
        stage('Test') {
            steps {
<<<<<<< HEAD
                sh './jenkins/scripts/test.sh'
=======
                sh '/usr/bin/sudo ./jenkins/scripts/test.sh'
>>>>>>> fe38dbff253b81e0dca20f9d326410bdec6138ed
            }
        }
    }
}
