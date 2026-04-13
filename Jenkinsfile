pipeline {
    
    agent any

    parameters {
        choice(name: 'CHOICE', choices:['Choice 1', 'Choice 2', 'Choice 3'], description: 'Pick a choice')
        string(name: ' STRING_PARAM', defaultValue: 'Default string', description: 'This is a string parameter')
    }
    
    environment {
        MY_VAR = "Value of MY_VAR"
    }

    stages {
        stage('Hello stage') {
            steps {
                echo "Hello World, this is my first Jenkins pipeline using a variable: ${env.MY_VAR}"
            }
        }

        stage('Credentials stage single brackets: best way to use credentials') {
            steps {
                withCredentials([string(credentialsId: 'my-secret', variable: 'TOKEN')]) {
                    echo 'The secret token is: ${TOKEN}'
                }
            }
        }

        stage('Print parameters') {
            steps {
                echo "You selected: ${params.CHOICE}"
                echo "String parameter value: ${params.STRING_PARAM}"
            }
        }
    }
}
