pipeline {
    agent any
    
    stages {
        stage('check k8s') {
            steps {
                sh 'kubectl get all --namespace flask-space'
            }
        }
        stage('Falsk-deploy') {
            steps {
                sh 'kubectl apply -f flask-deployment.yaml'
            }
        }
    }
}