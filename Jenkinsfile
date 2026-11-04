
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code checked out'
            }
        }

        stage('User Service') {
            steps {
                echo 'Building User Service'
            }
        }

        stage('Product Service') {
            steps {
                echo 'Building Product Service'
            }
        }

        stage('Order Service') {
            steps {
                echo 'Building Order Service'
            }
        }

        stage('Build Completed') {
            steps {
                echo 'All microservice stages completed'
            }
        }
    }
}
