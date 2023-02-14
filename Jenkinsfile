pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Run build commands here
                sh 'g++ -o PES1UG20CS487 new.cpp'
                build 'item:"PES1UG20CS487-1"'
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
            }
        }
        stage('Push') {
            steps {
                sh 'git add new.cpp'
                sh 'git commit -m "Add new file"'
                sh 'git push'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
