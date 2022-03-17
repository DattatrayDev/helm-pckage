pipeline {
    agent any

    stages {
        stage('add repo') {
            steps {
                sh 'https://dattatraydev.github.io/helm-pckage/'
            }
        }
         stage('Deploy') 
	{
        steps {
          kubernetesDeploy(
            kubeconfigId: 'KUBERNETES_CLUSTER_CONFIG',
            enableConfigSubstitution: true
          )
        }
    }
}
}
