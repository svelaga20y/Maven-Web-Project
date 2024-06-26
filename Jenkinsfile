node {
   
    stage('checkout') { 
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
    }
    stage('Build') {
       bat 'mvn package'
    }
    stage('test') {
        bat 'mvn test'
     }
	 stage('sonar-scanner') {
        bat 'mvn sonar:sonar -Dsonar.projectKey=test -Dsonar.host.url=http://localhost:9000 -Dsonar.login=d6f3f9a133e662198bcd324ce891e5ce7384e66b'
     }
}
  
