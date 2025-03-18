pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', 
                    branches: [[name: 'main']], 
                    userRemoteConfigs: [[url: 'https://github.com/Akmal79/PES1UG23CS805_Jenkins.git']]
                ])
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG23CS805-1'
                sh 'g++ ./main/hello.cpp -o ./output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stageeeeeeeeeeeenunuunijmi('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
