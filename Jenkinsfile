pipeline {
    agent any

    stages {
        stage('add repo') {
            steps {
                sh 'https://github.com/DattatrayDev/helm-pckage.git'
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
