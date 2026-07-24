pipeline {
    agent any

    stages {
        stage('git pull') {
            steps {
                git url: 'https://github.com/siu92/GitOps.git', branch: 'main'
            }
        }
        stage('k8s deploy') {
            steps {
                sh '/var/jenkins_home/kubectl apply -f deployment.yaml'
            }
        }
    }
}
