pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Compiling Java program...'
                bat 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Java program...'
                bat 'java HelloWorld'
            }
        }

        stage('Package') {
            steps {
                bat 'echo Build Number: %BUILD_NUMBER% > build-info.txt'
                bat 'echo Build executed on %DATE% %TIME% >> build-info.txt'
            }
        }
    }

    post {
        success {
            echo 'Java program tested successfully!'
        }
    }
}