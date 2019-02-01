node ('master') {
    stage ('Compile Stage') {
        bat 'mvn clean install'
    }

    stage ('Testing Stage') {
        bat 'mvn test'
    }

    stage('Generate HTML report') {
        cucumber buildStatus: "UNSTABLE",
                fileIncludePattern: '**/cucumber.json',
                sortingMethod: 'ALPHABETICAL',
                jsonReportDirectory: 'target'
    }
    stage('Email'){
        emailext body: '''Build Execution Completed, Checkout + Test + Reporting''', 
                        subject: 'Build Execution Completed', 
                        to: 'gbn.bb10@gmail.com'
    }
}
