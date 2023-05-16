pipeline {
    agent any
    stages {
        stage('check-secrets') {
            steps {
                sh 'rm trufflehog || true'
                sh 'docker run gesellix/trufflehog --json https://github.com/MukulG27/pipeline-practice.git > trufflehog'
                sh 'cat trufflehog'
            }
        }
        stage('SAST') {
            steps {
                sh 'rm mobsflog || true'
                sh 'docker run opensecurity/mobsfscan --json InsecureBankv2.apk > mobsflog'
                sh 'cat mobsflog'
            }
        }
        stage('build') {
            steps {
                sh 'python3 --version'
            }
        }
    }
}
