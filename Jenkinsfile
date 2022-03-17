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
				kubernetesDeploy(
                                   configs: 'index.yaml' ,
                                   kubeconfigId: 'KUBERNETES_CLUSTER_CONFIG' ,
                                   enableConfigSubstitution: true 
				)
			}
              }
    }
}
