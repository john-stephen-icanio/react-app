pipeline {
    agent {
        node {
            label 'jenkins-test1'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                    npm install
                    pm2 start --name jenkins_test "npm start" 
                '''
            }
        }
    }
}
