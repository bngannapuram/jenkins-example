pipeline {
    agent any
    stages {
        stage ('Compile Stage') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage ('Testing Stage') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Cucumber report') {
            steps {
                cucumber buildStatus: "UNSTABLE", 
                        fileIncludePattern: '**/cucumber.json',
                        jsonReportDirectory: 'target'
            }   
        }
    }
}
