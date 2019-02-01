pipeline {
    agent any

    stages {
        stage ('Checkout') {
            steps {
                git 'https://github.com/bngannapuram/jenkins-pipeline-maven.git'
            }
        }

        stage ('Compile') {
            steps {
                withMaven(maven : 'maven_3_6_0') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing') {
            steps {
                withMaven(maven : 'maven_3_6_0') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deploy') {
            steps {
                withMaven(maven : 'maven_3_6_0') {
                    bat 'mvn deploy'
                }
            }
        }
    }
}
