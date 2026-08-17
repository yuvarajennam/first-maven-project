pipeline {

    agent any

    tools {
        jdk 'JDK-21'
        maven 'Maven-3.9.16'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

    }

    post {

        success {
            echo 'Maven build completed successfully! 🎉'
        }

        failure {
            echo 'Maven build failed. Check the console output.'
        }

    }
}