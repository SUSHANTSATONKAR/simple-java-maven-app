
pipeline {
    agent any
    
    stages {
        stage('Fetch Code') {
            steps {
                echo 'Fetching code'
                git 'https://github.com/helpingpeopletolearn/galaxy-app.git'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies'
                sh 'sudo apt update'
                sh 'sudo apt-get install -y apache2'
            }
        }
        
        stage('Deploy App') {
            steps {
                echo 'Deploying app'
                sh 'sudo cp -r * /var/www/html'
            }
        }
    }
}
