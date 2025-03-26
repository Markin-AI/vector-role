pipeline {
    agent {
        label 'agent'
    }
    stages {
        stage ('Copy Git repo') {
            steps {
                git branch: 'main', credentialsId: '8969c6e7-68ba-45fa-96c0-0aba57754e2b', url: 'git@github.com:Markin-AI/vector-role.git'
            }
        }
        stage ('Run molecule test') {
            steps {
                dir('vector-role') {
                    sh 'molecule test'
                }
            }
        }
    }
}