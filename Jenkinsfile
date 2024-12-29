pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/BahaaAhmed-Hub/SimpleTodo.git'
            }
        }
        stage('Build Backend') {
            steps {
                dir('backend') {
                    echo "Hello" 
                    //sh 'mvn clean package'
                    sh 'export MAVEN_HOME=/opt/maven'
                    sh 'export PATH=$PATH:$MAVEN_HOME/bin'
                    sh 'mvn --version'
                }
            }
        }
        /*stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'mvn sonar:sonar'
                }
            }
        }
        stage('Build Docker Images') {
            steps {
                dir('backend') {
                    sh 'docker build -t your-dockerhub-user/backend:latest .'
                }
                dir('frontend') {
                    sh 'docker build -t your-dockerhub-user/frontend:latest .'
                }
            }
        }
        stage('Push Docker Images') {
            steps {
                sh 'docker push your-dockerhub-user/backend:latest'
                sh 'docker push your-dockerhub-user/frontend:latest'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/deployment-backend.yaml'
                sh 'kubectl apply -f k8s/deployment-frontend.yaml'
            }
        }
   */ }
}
