pipeline {
    agent any  

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o output main.cpp' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh './output'  
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying...'
                    echo 'Deployment Successful'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed! Check logs for errors.'
        }
    }
}
