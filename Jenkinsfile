pipeline {
    agent any

    tools {
        git 'git'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
    }

    post {
        success {
            mail to: 'brightnwankwo14@gmail.com',
                 subject: "Build Success",
                 body: "MediTrack deployed successfully"
        }
        failure {
            mail to: 'brightnwankwo14@gmail.com',
                 subject: "Build Failed",
                 body: "Check Jenkins immediately"
        }
    }
}
