pipeline {
    agent any

    stages {
        stage('Login to Docker Hub') {
            steps {
                // Login to Docker Hub using credentials
                withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    script {
                        sh 'echo "${PASSWORD}" | docker login -u "${USERNAME}" --password-stdin'
                    }
                }
            }
        }

        stage('Checkout Code') {
            steps {
                // Clone the repository from the master branch
                git branch: 'master', url: 'https://github.com/mostafaG95/Spring-BM.git'
            }
        }

        stage('Unit Tests') {
            steps {
                script {
                    // Run unit tests using Gradle
                    sh './gradlew test'
                }
            }
        }

        stage('Lint Code') {
            steps {
                script {
                    // Lint the code using Checkstyle for Gradle
                    sh './gradlew check'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Docker build step
                    sh 'docker build . -f Dockerfile -t mostafag95/app3'
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                script {
                    // Push the Docker image to Docker Hub
                    sh 'docker push mostafag95/app3'
                }
            }
        }
    }
}
