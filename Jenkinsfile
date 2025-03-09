// node {
//    def mvnHome = tool name: 'MAVEN', type: 'maven'
   
//     stage('checkout') { 
//         git 'https://github.com/svelaga20y/Maven-Web-Project.git'
//     }
    
//     stage('build') {
//        sh "${mvnHome}/bin/mvn clean package"
//     }

// }

pipeline{
    agent any
    tools{
        maven 'MAVEN1'
    } 
    stages{
        stage('checkout') { 
            steps{
                git 'https://github.com/svelaga20y/Maven-Web-Project.git'
            }
        }
    
        stage('compile') {
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('build'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
  
