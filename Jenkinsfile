pipeline {
    agent any
    parameters {
        string(name: 'dev', defaultValue: '/Applications/MAMP/htdocs/jenkin_project', description: 'Dev server')
        string(name: 'prod', defaultValue: '/usr/local/var/www/jenkin_project', description: 'Prod Server')
    }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo "Testing...."
            }
        }

        stage('Deploy') {
            parallel {
                stage('deploy to dev'){
                    sh 'cp * ${params.dev}'
                }
                stage('deploy to prod'){
                    sh 'cp * ${params.prod}'
                }
            }
        }
    }
}
