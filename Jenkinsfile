pipeline {
    agent any
    stages {
	stage ('Pull Build Code'){
	   steps {
                  parallel("RMS": {
                    echo "hello RMS"
                },      
                        "MGS": {
                            echo "Hello MGS"
                        }
                )

	   }
        }
        stage('Build Docker Image') {
            steps {
                parallel("RMS Docker": {
                    echo "Build"
                    echo "Push"
                },
                        "MGS Docekr build": {
                            echo " Build MGS"
                            echo "Push MGS"
                        }
                )
            }
        }
        stage('Deploy') {
            steps {
                parallel("RMS": {
                    echo "hello RMS"
                },
                        "MGS": {
                            echo "Hello MGS Deploy"
                        },
                        "RMN": {
                            echo "Hello RMNi Deploy"
                        }
                )
            }
        }
    }
}
