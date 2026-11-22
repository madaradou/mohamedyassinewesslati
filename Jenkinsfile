pipeline {
    agent any
    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/madaradou/mohamedyassinewesslati.git',
                    credentialsId: 'github-cred'
            }
        }
        stage('Build Maven') {
            steps {
                sh 'mvn compile'
            }
        }
    }
}
