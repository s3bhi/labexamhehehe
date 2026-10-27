
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the Java project...'
                bat '"C:\\Users\\Subhi Jose\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin\\mvn.cmd" clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running test cases...'
                bat '"C:\\Users\\Subhi Jose\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin\\mvn.cmd" test'
            }
        }
    }

    post {
        success {
            echo 'SUCCESS: Build and tests completed!'
        }

        failure {
            echo 'FAILURE: Build or tests failed!'
        }

        always {
            echo 'Jenkins pipeline execution finished.'
        }
    }
}
