pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    // Docker login
                    bat 'docker login -u harshini45 -p HARSHINI@2005'

                    // Build and push Docker image
                    bat 'docker build -t w9-dd-app:latest .'
                    bat 'docker tag w9-dd-app:latest harshini45/w9-dd-app:latest'
                    bat 'docker push harshini45/w9-dd-app:latest'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Skipping Deploy stage — Minikube is not installed on this Jenkins server.'
                }
            }
        }
    }
}
