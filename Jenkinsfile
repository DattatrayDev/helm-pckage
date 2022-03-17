pipeline {
    agent any
    stages {
        stage('add repo') {
            steps {
		    sh "helm repo add helm-pckage https://dattatraydev.github.io/helm-pckage/"
            }
        }
	    stage("Deploy") {
                        steps {
				sh "helm install sample-application ./helm-package"
				
			}
              }
    }
}
