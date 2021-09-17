pipeline {
    agent any
    stages {
        stage('git repo & clean')  {
            steps {
              // bat "rmdir  /s /q gitpjt"
                bat "git clone https://github.com/ganeshrajnokia/gitpjt.git"
                bat "mvn clean -f gitpjt"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f gitpjt"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f gitpjt"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f gitpjt"
            }
        }
    }
}
