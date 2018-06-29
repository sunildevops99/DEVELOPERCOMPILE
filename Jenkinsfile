env.mvnHome = '/usr/share/maven3'
node('mavenagent') {
   
   
   stage('Preparation') { // for display purposes
      
      git 'https://github.com/sunildevops99/DEVELOPERCOMPILE.git'
        
      
   }
   stage('Build') {
      
      if (isUnix()) {
         sh "'${mvnHome}/bin/mn' clean install"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
   stage('publish') {
     echo 'vdjhvbhjdsb'
   }
   

}
