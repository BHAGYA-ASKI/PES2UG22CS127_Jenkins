pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ program.cpp -o program.out'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './program.out'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
