pipeline {
    agent any

    stages {
        stage('Building') {
            steps {
                echo 'Building the Dev project'
            }
        }
         stage('Testing') {
            steps {
                checkout(git branch: 'main', changelog: false, poll: false, url: 'https://github.com/jkabirqa/Selenium4Test.git')
                sh 'mvn clean test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the code on Staging server'
            }
        }
    }
}
