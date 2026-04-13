pipeline{
    agent any

    parameters{
        choice(name: 'DEPLOY_ENV', choices: ['dev', 'staging', 'prod'])
    }

    stages{
        stage('Deploy'){
            steps{
                withCredentials([string(credentialsId: 'API_KEY', variable: 'API_KEY')]){
                    echo "Ciao Questo è il deploy usando la API_KEY: ${API_KEY}"
                    echo "L'ambiente di sviluppo è: ${params.DEPLOY_ENV}"
                }
            }
        }
    }
}