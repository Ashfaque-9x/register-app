pipline{
    agent { lable 'Jenkins-Agent'}

    tools{
        jdk 'Java17'
        maven 'Maven3'
    }

    stages{
        stage('Cleanup Workspace'){
            steps{
                cleanWs()
            }
        }
        stage('SCM Checkout'){
            steps{
                git branch: 'main', credentialsId: 'gitpass', url: 'https://github.com/AASAITHAMBI57/register-app-ass.git'
            }
        }
        stage('mvn compile'){
            steps {
            sh 'mvn clean compile' 
            }
        }
        stage('mvn test'){
            steps {
            sh 'mvn test' 
            }
        }
    }
}
