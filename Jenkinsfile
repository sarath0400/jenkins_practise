pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout Code from Develop') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/develop']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/sarath0400/jenkins_practise.git'
                    ]]
                ])
            }
        }

        stage('Show Pulled Files') {
            steps {
                sh 'echo "Files pulled into Jenkins workspace:"'
                sh 'ls -l'
            }
        }
    }
}
