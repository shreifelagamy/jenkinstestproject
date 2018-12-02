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
