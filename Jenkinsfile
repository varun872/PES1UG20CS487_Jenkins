pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Run build commands here
                sh 'g++ -o PES1UG20CS487 ./main/new.cpp'
                build job:"PES1UG20CS487-1"
            }
        }
        stage('Test') {
            steps {
                // Run test commands here
                sh './PES1UG20CS487'
            }
        }
        stage('Deploy') {
            steps {
                // Run deployment commands here
                sh 'echo "Deployed!!"'
            }
        }
    }
    
    post {
        always {
            sh 'echo "Pipeline finished"'
        }
        failure {
            sh 'echo "Pipeline failed"'
        }
    }
}
