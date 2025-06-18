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
                git 'https://github.com/Oren1984/hello-python.git'
            }
        }
    }
}
