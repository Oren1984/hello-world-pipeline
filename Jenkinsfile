pipeline {
    agent { label 'my-agent' }  // זה הכרחי!
    
    stages {
        stage('Print Message') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-world-pipeline .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 hello-world-pipeline'
            }
        }

        stage('Docker Compose Up') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}

