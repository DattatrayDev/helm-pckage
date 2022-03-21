pipeline {
    agent any
    stages {
        stage('add repo') {
            steps {
		    sh "export KUBECONFIG=/etc/rancher/k3s/k3s.yaml"
		    sh "helm install sample-application ."
            }
        }
    }
}
