node ('master') {
    stage('Checkout'){
        git 'https://github.com/bngannapuram/jenkins-pipeline-maven.git'
    }

    stage ('Compile Stage') {
        bat 'mvn clean compile'
    }

    stage ('Testing Stage') {
        bat 'mvn test'
    }

    stage ('Deployment Stage') {
        bat 'mvn deploy'
    }
}
