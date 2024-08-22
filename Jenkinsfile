pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning the repository...'
                git branch: 'main', url: 'https://github.com/talelekaustubh/TECHNOCRAFTZ.git'
            }
        }


        stage('Deploy') {
            steps {
                echo 'Deploying the static HTML site...'
                // Simulate deployment; replace with actual deployment commands
                sh 'echo "Deploying to web server or cloud storage..."'
                // Example for deploying to an S3 bucket (if you use AWS S3):
                // sh 'aws s3 sync . s3://my-bucket-name --delete'
                // Example for deploying to an FTP server:
                // sh 'lftp -e "mirror -R ./ /path/on/server" -u ftpuser,ftppassword ftp://ftpserver.com'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up workspace...'
            cleanWs()
        }

        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
