pipeline {
    agent any
    stages {
        stage('add repo') {
            steps {
		    sh "helm install sample-application ."
            }
        }
    }
}
