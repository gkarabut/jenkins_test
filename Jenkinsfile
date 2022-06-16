#!groovy

pipeline {
    agent any
      environment {
          BUILD_NUMBER = '9999'
      }
     
      stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
          post {
              always {
                  archiveArtifacts env.BUILD_NUMBER+'Jenkinsfile'
              }
          }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh "ls -lah"            
            }
        }
    }
}
