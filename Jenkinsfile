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
        stage('Test') {
    steps {
        sh './non_existent_exec' // This will cause an error
    }
}

    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
