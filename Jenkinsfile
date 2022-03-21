pipeline {
    agent any
    stages {
        stage('minikube') {
            steps {
		    sh "minikube start"
		    sh "helm install sample ."
		    sh "minikube service myapp-service"
            }
        }
    }
}
