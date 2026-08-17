pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/VrushaliDudhaneJob/Jenkinsfiledemorepo.git'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'

                sh '''
                    rm -f /var/www/html/index.html
sudo cp -r ./README.md ./index.html ./script.js ./style.css /var/www/html/
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment successful!'
        }

        failure {
            echo 'Deployment failed!'
        }
    }
}
