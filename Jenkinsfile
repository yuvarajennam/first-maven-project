pipeline {

    agent any

    tools {
        jdk 'JDK-21'
        maven 'Maven-3.9.16'
    }

    stages {

        stage('Build & Test') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java -cp target\\classes com.yuvaraj.App'
            }
        }
    }

    post {

        success {
            echo 'Maven build, tests and application run completed successfully! 🎉'
        }

        failure {
            echo 'Build failed. Check the console output.'
        }
    }
}