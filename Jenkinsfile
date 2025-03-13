pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling main.cpp...'
                sh '''
                    g++ -o PES1UG22AM110-1 main.cpp
                    echo "Build completed successfully!"
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh '''
                    ./PES1UG22AM110-2
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage placeholder...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
