pipeline {
    agent any // Change to 'any' if docker-agent isn't working

    stages {
        stage('Show Info') {
            steps {
                sh '''
                echo "Name: Pavan Koushik"
                echo "Roll No: SE22UCSE326"
                printenv
                '''
            }
        }

        stage('Create File') {
            steps {
                sh '''
                echo "This is Job F running from a Jenkinsfile in Git." > data.txt
                cat data.txt
                '''
            }
        }
    }
}
