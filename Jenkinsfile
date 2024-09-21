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

        stage('Build Docker Image') {
            steps {
                // Clone the repository from the master branch
                git branch: 'master', url: 'https://github.com/mostafaG95/Spring-BM.git'

                // Docker build step
                script {
                    sh 'docker build . -f Dockerfile -t mostafag95/app --network host'
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                script {
                    // Push the Docker image to Docker Hub
                    sh 'docker push mostafag95/app'
                }
            }
        }
    }
}
