pipeline {
    agent any
    stages {
        stage('minikube') {
            steps {
		    sh "minikube stop"
		    sh "minikube delete"
            }
        }
	 
    }
}
