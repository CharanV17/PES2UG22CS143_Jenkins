pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_exec hello.cpp' // Compile C++ file
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec' // Run the compiled program
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
