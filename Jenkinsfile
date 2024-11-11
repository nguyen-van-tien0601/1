pipeline {
    agent any 
    
    stages {
        stage('checkout scm') {
            steps{
                checkout scm
            }
        }
        stage('Build') { 
            steps { 
                sh 'echo "hello"' 
            }
        }
        stage('Test'){
            steps {
                sh 'echo "good bye every"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "a"'
            }
        }
    }
}
