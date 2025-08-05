pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mg2412/jenkins-ci-cd-lab.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.war', fingerprint: true
            }
        }
    }
}
