pipeline {
    agent any

    triggers {
        pollSCM('*/30 * * * *')
    }

    stages {
        stage("Clone") {
            steps {
                script {
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/danielshine1/MySoftware.git']]])
                }
            }
        }

        stage("Run Files") {
            steps {
                script {
                    sh 'python click.py'
                    sh 'python newscreen.py'
                }
            }
        }
    }
}
