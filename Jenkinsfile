pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'echo "hello"' 
            }
        }
        stage('Test'){
            steps {
                sh 'echo "good"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "test"'
            }
        }
    }
}