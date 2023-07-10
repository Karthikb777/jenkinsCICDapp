properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any

    stages {
        stage("pull latest changes") {
              steps {
                checkout([
                 $class: 'GitSCM',
                 branches: [[name: 'main']],
                 userRemoteConfigs: [[
                    url: 'git@github.com:Karthikb777/jenkinsCICDapp.git',
                    credentialsId: '',
                 ]]
                ])
            }
        }

        stage("build docker images") {
            echo "built "
        }

        stage("push docker images") {
            echo "pushed"
        }

        stage("bring cluster down") {
            echo "down"
        }

        stage("deploy latest images") {
            echo "deployed"
        }
    }
}