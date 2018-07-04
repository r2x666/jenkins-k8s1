pipeline {
    agent any
    stages {
      stage ('Pull Git'){
          steps {
               git credentialsId: 'GIT-Login', url: 'https://github.com/r2x666/jenkins-k8s1'
            }
        }
        stage ('Build docker image'){
            steps {
                sh 'docker build -t r2x666/jenkins-docker:3.0.0 .'
            }
         }
        stage ('Push docker image'){
            steps {
                withCredentials([string(credentialsId: 'docker-pwd', variable: 'DockerPWD')]) {
    		  sh "docker login -u r2x666 -p ${DockerPWD}"
		}
                sh 'docker push -t r2x666/jenkins-docker:3.0.0 .'
            }
        }
    }
}
