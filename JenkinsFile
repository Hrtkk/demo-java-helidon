pipeline {
    agent any;

    environment {
        CC = 'clang'
    }

    parameters {
        string(NAME: 'Greeting', defaultValue: 'Hello', DESCRIPTION: 'How should I greet the World?')
    }

    stages {
        stage ('Experimenting') {
            environment {
                DEBUG_FLAGS = '-g'
            }

            steps {
                echo 'Experimenting...'
                echo "${params.Greeting} World"
                echo "Printing some environment variable: BUILD ID: ${env.BUILD_ID} Jenkins Url: ${env.JENKINS_URL}"
                sh 'printenv'
            }
        }

        stage ('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage ('Test') {
            step {
                echo 'Testing...'
            }
        }

        stage ('Deploy') {
            step {
                echo 'Deploying...'
            }
        }
    }
}