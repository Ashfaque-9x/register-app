pipeline{
    agent { label ' Jenkins-Agent' }

    stages{
        stage("Cleanup Workspace"){
            steps{
                cleanWs()
            }
        }
        stage("Checkout from SCM"){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitPass', url: 'https://github.com/AASAITHAMBI57/register-app-ass.git']])
            }
        }
    }
}
