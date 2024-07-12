pipeline {
    agent any
    parameters {
      string defaultValue: 'fritz', description: 'Enter firstname', name: 'firstname '
      string defaultValue: 'mbog', description: 'Enter lastname ', name: 'lastname '
    }


    stages {
        stage('welcome') {
            steps {
                echo "hi ${params.firstname} ${params.lastname}, welcome"
            }
        }
        
        
    }
}
