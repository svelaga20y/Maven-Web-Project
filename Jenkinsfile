node {
    def mvnHome
    stage('checkout') { 
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
        mvnHome = tool 'MAVEN3'
    }
    stage('Build') {
        // Run the maven build
        withEnv(["MVN_HOME=$mvnHome"]) {
            if (isUnix()) {
                sh '"$MVN_HOME/bin/mvn" clean package'
            } else {
                bat(/"%MVN_HOME%\bin\mvn" clean package/)
            }
        }
    }
    stage('Install') {
        // Run the maven build
        withEnv(["MVN_HOME=$mvnHome"]) {
            if (isUnix()) {
                sh '"$MVN_HOME/bin/mvn" clean install'
            } else {
                bat(/"%MVN_HOME%\bin\mvn" clean install/)
            }
        }
    }
    stage('test') {
        // Run the maven build
        withEnv(["MVN_HOME=$mvnHome"]) {
            if (isUnix()) {
                sh '"$MVN_HOME/bin/mvn" clean test'
            } else {
                bat(/"%MVN_HOME%\bin\mvn" clean test/)
            }
        }
    }
  
    
}
