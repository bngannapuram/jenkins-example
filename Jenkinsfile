pipeline {
    agent any
    stages {
        stage ('Compile Stage') {
            bat 'mvn clean install'
        }

        stage ('Testing Stage') {
            bat 'mvn test'
        }

        stage('Cucumber report') {
            cucumber buildStatus: "UNSTABLE", 
                    fileIncludePattern: '**/cucumber.json',
                    jsonReportDirectory: 'target'
        }
    }
}
