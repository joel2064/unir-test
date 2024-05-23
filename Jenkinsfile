pipeline{
    agent any

    stages{
        stage('Hello'){
            steps{
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master' ]],
                    extensions: scm.extensions,
                    userRemoteConfigs: [[
                        url: 'https://github.com/ramosunir/unir-test.git'
                    ]]
                ])
            }
        }
    }
}