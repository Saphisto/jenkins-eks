pipeline {
    agent any
    
    stages {
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