pipeline {
    agent any
    stages {
      stage ('Pulling Code'){
          steps {
               git credentialsId: 'GIT-Login', url: 'https://github.com/r2x666/jenkins-k8s1'
            }
        }
        stage ('Build docker image'){
            steps {
                sh 'docker build -t r2x666/jenkins:1.0.0 .'
            }
        }
    }
}
