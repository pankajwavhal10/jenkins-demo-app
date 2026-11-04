
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/pankajwavhal10/jenkins-demo-app.git',
                    credentialsId: 'Github-Cred'
            }
        }

        stage('Build') {
            steps {
                echo 'Nothing to build - Static HTML application'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Archiving application artifacts...'

                archiveArtifacts artifacts: 'index.html',
                                 fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'Demo deployed successfully!'
        }

        failure {
            echo 'Deployment failed!'
        }

        always {
            echo 'Jenkins pipeline execution completed.'
        }
    }
}
