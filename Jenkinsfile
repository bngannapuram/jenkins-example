pipeline {
    agent any

    stages {
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
