node('slave2') {
   
    stage('checkout') { 
        git 'https://github.com/praveenkumar1290/Maven-Web-Project.git'
    }
    
    stage('build') {
        sh 'mvn package'
    }

}
  
