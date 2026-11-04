
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Source code checked out successfully'
            }
        }

        stage('Check Environment') {
            steps {
                sh '''
                    java -version
                    mvn -version
                '''
            }
        }

        stage('Build User Service') {
            steps {
                dir('user-service') {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }

        stage('Build Product Service') {
            steps {
                dir('product-service') {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }

        stage('Build Order Service') {
            steps {
                dir('order-service') {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }
    }

    post {
        success {
            echo 'All three microservices built successfully!'
        }
        failure {
            echo 'Microservices build failed. Check console output.'
        }
    }
}
