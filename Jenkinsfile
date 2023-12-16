pipeline{
    agent { label ' Jenkins-Agent' }

    tools{
        jdk 'Java11'
        maven 'Maven3'
    }

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
        stage('mvn compile'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('mvn test'){
            steps{
                sh 'mvn test'
            }
        }
    }
}
