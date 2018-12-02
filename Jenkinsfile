pipeline {
    agent any
    stages {
        stage('Init') {
            steps {
               echo "Testing...."
            } 
        }

        stage('Build') {
            steps {
                echo "Asking...."
                input message: 'Do you want to complete?'
                echo "Building..."
                build job: 'staging'
            }
        }

        stage('Deploy') {
            steps {
                echo "Code deploied.... "
            }
        }
    }
}
