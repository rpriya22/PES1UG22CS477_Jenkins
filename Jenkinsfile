pipeline {
    agent any
   
    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "Building the C++ application..."
                    g++ -o PES1UG22CS477-1 main.cpp
                    echo "Build stage completed."
                '''
            }
        }
       
        stage('Test') {
            steps {
                sh '''
                    echo "Testing the C++ application..."
                    ./PES1UG22CS477-1
                    echo "Test stage completed."
                '''
            }
        }
       
        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying the application..."
                    echo "Deployment completed successfully."
                '''
            }
        }
    }
   
    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline completed successfully'
        }
    }
}
