node {
    
   def mvnHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      //git credentialsId: 'github', url: 'git@github.com:vijaynauti/jenkins_test.git'
       git credentialsId: 'GITHUB_TEST', url: 'git@github.com:vijaynauti/jenkins_test.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = tool 'mvn3'
      env.JAVA_HOME="${tool 'jdk8'}"
      env.PATH="${env.JAVA_HOME}/bin:${env.PATH}"
      
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -f api-gateway/pom.xml -Dmaven.test.failure.ignore clean package"
          sh "pwd"
          sh "whoami"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      junit '**/api-gateway/target/surefire-reports/*.xml'
      archiveArtifacts 'api-gateway/target/*.jar'
   }
}
 
