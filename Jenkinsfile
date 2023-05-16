pipeline {
    agent any
    stages {
        stage('check-secrets') {
            steps {
                sh 'rm trufflehog || true'
                sh 'sudo docker run gesellix/trufflehog --json https://github.com/MukulG27/pipeline-practice.git > trufflehog'
                sh 'cat trufflehog'
        stage('build') {
            steps {
                
            }
        }
    }
}
