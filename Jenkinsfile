pipeline {
    
    agent any
    
    envirnoment {
        MY_VAR = "Value of MY_VAR"
    }

    stages {
        stage('Hello stage') {
            steps {
                echo "Hello World, this is my first Jenkins pipeline using a variable: ${env.MY_VAR}"
            }
        }
    }
}
