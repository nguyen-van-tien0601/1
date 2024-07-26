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
                sh 'echo "good bye every"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'python app.py'
            }
        }
    }
}
