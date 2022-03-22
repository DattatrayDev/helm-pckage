pipeline {
    agent any
    stages {
        stage('minikube') {
            steps {
		    sh "minikube start"
            }
        }
	    stage('install') {
            steps {
		    sh "helm install sample ."
            }
        }
	    stage('url') {
            steps {
		    sh "minikube service myapp-service --url"
            }
        }
    }
}
