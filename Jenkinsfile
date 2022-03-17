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
				container('helm') {
           withCredentials([file(credentialsId: 'project-credentials', variable: 'PULL_KEYFILE')])
	{
            sh """
            gcloud auth activate-service-account --key-file=${PULL_KEYFILE} --project project-name
            gcloud container clusters get-credentials cluster-name --zone us-east1
            kubectl create namespace ${NAMESPACE} --dry-run -o yaml | kubectl apply -f -
            """
            helm upgrade --install release-name .
          }
        }
			}
              }
    }
}
