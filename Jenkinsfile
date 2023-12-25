pipeline{
    agent any
/*    
    tools {
         maven 'maven'
         jdk 'java'
    }
*/
    stages{
        stage('Git Checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'mygithub', url: 'https://github.com/hemantgoli/devops-mvn-demo.git']]])
            }
        }
        stage('mvn clean'){
            steps{
               bat 'mvn clean'
            }
        }
        stage('mvn compile'){
            steps{
               bat 'mvn compile'
            }
        }
        stage('mvn package'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
