stages {
    stage('Checkout') {
        steps {
            git url: 'https://github.com/pankajwavhal10/jenkins-demo-app.git',
                credentialsId: 'Github-Cred'
        }
    }
    stage('Build') {
        // No build needed for static HTML – just copy files
        steps { echo 'Nothing to build' }
    }
    stage('Deploy') {
        // Deploy to a folder served by IIS/Apache/NGINX, or just archive
        steps {
            // Example: archive artifacts for later download
            archiveArtifacts artifacts: 'index.html', fingerprint: true
        }
    }
}

post {
    success { echo '✅ Demo deployed successfully' }
    failure { echo '❌ Deployment failed' }
}
}
