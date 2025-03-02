node {
   def mvnHome = tool name: 'MAVEN', type: 'maven'
   
    stage('checkout') { 
        git 'https://github.com/svelaga20y/Maven-Web-Project.git'
    }
    
    stage('build') {
       sh "${mvnHome}/bin/mvn clean package"
    }

}
  
