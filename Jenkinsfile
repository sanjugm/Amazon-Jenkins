pipeline {
    agent any
    
    stages {

        stage('Compile') {
            steps {
                bat 'mvn compile'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

    }

    post {
        success {
            echo 'Build success'
        }
        failure {
            echo 'Failure in the build'
        }
    }
}
