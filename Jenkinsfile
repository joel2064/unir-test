pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master' ]],
                    extensions: scm.extensions,
                    userRemoteConfigs: [[
                        url: 'https://github.com/joel2064/unir-test.git'
                    ]]
                ])
            }
        }
        stage('Build'){
            steps{
                sh 'python3 ./app/api.py'
            }

        }
    }
}