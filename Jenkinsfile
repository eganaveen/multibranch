pipeline {
    agent any
    parameters{
        choice(name: 'version', choices: ['1.0.0','2.0.0','3.0.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when{
                expression{
                    params.executeTests
                }
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "Deploying version ${params.version}"
            }
        }
    }
}
