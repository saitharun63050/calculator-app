pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK21'
    }

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Code checked out from SCM'
            }
        }

        stage('Build & Test') {
            steps {
                sh 'mvn clean test'
            }
        }
    }

    post {
        success {
            echo 'Build and Tests Successful!'
        }
        failure {
            echo 'Build or Tests Failed!'
        }
    }
}
