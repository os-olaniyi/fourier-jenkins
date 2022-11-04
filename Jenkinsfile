pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Git Clone') {
            steps {
                echo 'Building Something'
                git credentialsId: 'GitHubCred', url: 'https://github.com/os-olaniyi/fourier-jenkins.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building Something'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Something'
            }
        }
        stage('Test01') {
            steps {
                echo 'Testing'
            }
        }
      stage ('Test02') {
        steps {
            echo 'Testing another'
        }
      }
        stage('Release') {
            steps {
                echo 'Releasing Something'
            }
        }
    }
}
