pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    set -e  # Stop the script if any command fails
                    g++ -o PES1UG22CS477-1 pes1ug22cs477.cpp  # Compile the C++ file
                    chmod +x PES1UG22CS477-1  # Ensure it is executable
                    '''
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh '''
                    echo "Running the compiled program..."
                    ./PES1UG22CS477-1  # Execute the program
                    '''
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...' 
                // Add deployment steps here if needed
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed! Please check the logs.'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
