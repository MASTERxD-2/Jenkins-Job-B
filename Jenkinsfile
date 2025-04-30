pipeline {
    agent any // Change to 'any' for local agent

    environment {
        PROJECT_NAME = "My Jenkins Pipeline Project"
        AUTHOR = "Pavan Koushik"
        ROLL_NO = "SE22UCSE326"
    }

    stages {
        stage('Print Info') {
            steps {
                echo "Project: ${env.PROJECT_NAME}"
                echo "Author: ${env.AUTHOR}"
                echo "Roll Number: ${env.ROLL_NO}"
                echo "Job Name: ${env.JOB_NAME}"
                echo "Build Number: ${env.BUILD_NUMBER}"
            }
        }

        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/your-python-repo.git'
            }
        }

        stage('Run Python Script') {
            steps {
                sh 'python3 main.py' // Replace with your actual script
            }
        }

        stage('Save Output') {
            steps {
                sh 'echo "Sample output data" > data.txt'
                archiveArtifacts artifacts: 'data.txt', onlyIfSuccessful: true
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully!"
        }
        failure {
            echo "Pipeline failed. Please check logs."
        }
    }
}
