pipeline {
    agent any

    stages {
        stage ('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage ('Testing') {
            steps {
                bat 'mvn test'
            }
        }

        stage ('Deploy') {
            steps {
                bat 'mvn deploy'
                }
        }
    }
}
