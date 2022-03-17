pipeline {
    agent any
    stages {
        stage('add repo') {
            steps {
		    sh "helm repo add helm-package https://dattatraydev.github.io/helm-pckage/"
            }
        }
	    stage("Deploy") {
                        steps {
				sh "helm install helm-package my-application"
				)
			}
              }
    }
}
