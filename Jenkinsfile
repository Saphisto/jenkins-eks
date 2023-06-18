pipeline {
    agent any
    
    stages {
        stage('Build image') {
            steps {
                sh 'docker build -t flask-fronend:${params:flask_version} .'
            }
        }
        stage('Falsk-deploy') {
            steps {
                sh 'kubectl apply -f flask-deployment.yaml'
            }
        }
        stage('check k8s') {
            steps {
                sh 'kubectl get all --namespace flask-space'
            }
        }
    }
}