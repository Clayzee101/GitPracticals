pipeline {
    agent any

    stages {
        
        stage('Fetch') {
            steps {
                echo 'Fetching from Repo...'
                git 'https://github.com/Clayzee101/GitPracticals.git'
            }
        }
        stage('Build ') {
            steps {
                echo 'Building in Progress....'
                bat 'javac hello.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing in Progress....'
                bat 'java hello'
            }
        }
    }
     post{
            success{
                echo 'Pipeline build Seccessfully'
            }
            failure{
                echo 'Pipeline failed'
            }
        }
}
