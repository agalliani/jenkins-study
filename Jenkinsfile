pipeline {
    
    agent any
    
    environment {
        MY_VAR = "Value of MY_VAR"
    }

    stages {
        stage('Hello stage') {
            steps {
                echo "Hello World, this is my first Jenkins pipeline using a variable: ${env.MY_VAR}"
            }
        }

        stage('Credentials stage'){
            steps {
                withCredentials([string(credentialsID: 'my-secret', variable: 'TOKEN')]) {
                    echo "The secret token is: ${TOKEN}"
                }
            }
        }
    }
}
