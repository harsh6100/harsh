
    
pipeline {
    agent { docker 'maven' }
    stages {
        stage('compile stage') {
            steps {
                bat 'mvn compile'
            }
           
        }
        stage('test') {
            steps {
                bat 'mvn test'
            }
           
        }
    }
}



