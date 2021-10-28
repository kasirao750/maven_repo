pipeline {
    agent any

   tools {
        
        maven "maven_3.8"
     }

    stages {
        stage('SCM') {
            steps {
               
               git branch: 'main', changelog: false, credentialsId: '9b93ba8a-2d89-48d2-b050-e12e68e4fa21', poll: false, url: 'https://github.com/kasirao750/maven_repo.git'
              
            }
        }
        stage('Build') {
            steps {
                bat 'mvn deploy'
            }
        }
            }
        }
