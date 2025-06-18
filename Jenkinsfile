pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Print Message') {
            steps {
                echo 'Hello World'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // בונה את התמונה בשם hello-world-pipeline
                    sh 'docker build -t hello-world-pipeline .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // מריץ את הקונטיינר במצב detached עם פורט 5000 (כדוגמה)
                    sh 'docker run -d -p 5000:5000 --name hello-world-container hello-world-pipeline'
                }
            }
        }

        stage('Docker Compose Up') {
            steps {
                script {
                    // רץ docker-compose לפי הקובץ שנמצא בפרויקט
                    sh 'docker-compose up -d'
                }
            }
        }
    }
}
