pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'java'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/srikanthsince98/repo1.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn  package'
            }
        }
    }
}