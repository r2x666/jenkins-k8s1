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
        stage('one') {
            steps {
                parallel("first": {
                    echo "hello"
                },
                        "second": {
                            echo "world"
                        }
                )
            }
        }
        stage('two') {
            steps {
                parallel("first": {
                    echo "hello"
                },
                        "second": {
                            echo "world"
                        }
                )
            }
        }
    }
}
