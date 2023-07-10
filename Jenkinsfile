properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any

    stages {
        stage("pull latest changes") {
              steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/Karthikb777/jenkinsCICDapp.git' 
            }
        }

        stage("build docker images") {
            steps {
                echo "built again"
            }
        }
        

        stage("push docker images") {
            steps {
                echo "pushed again"
            }
        }

        stage("bring cluster down") {
            steps {
                echo "down"
            }
        }

        stage("deploy latest images") {
            steps {
                echo "deployed"
            }
        }
    }
}