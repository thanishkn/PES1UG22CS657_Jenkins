pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o hello_exec main/hello.cpp' // Compile the C++ program
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'exit 1'
                    //sh './hello_exec' // Run the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
