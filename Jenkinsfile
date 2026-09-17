pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Thamaraiselvan-26/Assessment_7_Project2.git'
            }
        }
        stage('Generate Exam Report') {
            steps {
                bat 'python app.py'
            }
        }
        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'exam_report.txt', fingerprint: true
            }
        }
    }
}
