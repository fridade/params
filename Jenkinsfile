pipeline {
    agent any
    parameters {
        string(defaultValue: 'fritz', description: 'Enter firstname', name: 'firstname')
        string(defaultValue: 'mbog', description: 'Enter lastname', name: 'lastname')
        choice choices: ['dev', 'qa', 'stage', 'prod'], description: 'choose the environment ', name: 'Area'
    }

    stages {
        stage('welcome') {
            steps {
                echo "hi ${params.firstname} ${params.lastname}, welcome"
            }
        }
        
        stage('deploy to dev') {
           when {
            expression {
                params.Area == "dev"
            }
            steps{
                echo 'Deploying to dev '
            }
           }
        }
        stage('deploy to stage') {
           when {
            expression {
                params.Area == "stage"
            }
            steps{
                echo 'Deploying to stage'
            }
           }
        }
        stage('deploy to prod') {
           when {
            expression {
                params.Area == "prod"
            }
            steps{
                echo 'Deploying to prod'
            }
           }
        }
    }
}
