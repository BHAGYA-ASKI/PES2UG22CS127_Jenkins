pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ program.cpp -o program.out'
            }
        }
        
        stage('Test') {
            steps {
                sh './program.out'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
