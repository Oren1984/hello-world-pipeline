pipeline {
    agent any

    stages {
        stage('Print Message') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Git Clone') {
            steps {
                 git branch: 'main', credentialsId: 'github-token', url: 'https://github.com/Oren1984/hello-world-pipeline.git'
            }
        }
    }
}
