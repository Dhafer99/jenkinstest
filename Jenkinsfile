pipeline {
    agent any

    triggers {
        // Polling every 20 seconds within each minute
        pollSCM('H/20 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                git branch: 'main', url: 'https://github.com/Dhafer99/jenkinstest.git'
            }
        }
        
        stage('Show Date') {
            steps {
                // Display the system date
                script {
                    def date = new Date()
                    echo "Current system date and time: ${date}"
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
    }
}
