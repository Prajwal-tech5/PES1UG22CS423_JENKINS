pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG22CS423-1 hello.cpp'
                echo 'Build stage completed'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG22CS423-1'
                echo 'Test stage completed'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment completed'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline succeeded'
        }
    }
}
