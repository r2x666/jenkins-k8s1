pipeline {
    agent any
    stages {
	stage ('Pull Code') {
	   steps {
		echo "Checkout SCM"
	   }
	stage ('Build') {
	   steps {
		echo "Build Code"
	   }
        stage('Test Windows') {
            steps {
                parallel("Win": {
                    echo "hello Windows"
                },
                        "second": {
                            echo "world"
                        }
                )
            }
        }
        stage('Test Unix') {
            steps {
                parallel("Unix Testing": {
                    echo "hello"
                },
                        "second": {
                            echo "Unix"
                        }
                )
            }
        }
    }
}
