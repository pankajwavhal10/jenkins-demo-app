pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting static HTML application build...'
                echo 'Nothing to compile - Static HTML application'
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
            echo 'Demo application pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline execution failed!'
        }

        always {
            echo 'Jenkins pipeline execution completed.'
        }
    }
}
