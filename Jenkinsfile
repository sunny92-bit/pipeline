pipeline {

agent any

stages {
stage ('SCM') {
         steps {
                 echo "git pull my code"
         }
}
stage ('Deploy') {
         steps {
                echo "deploy my code"
         }  
}
stage ('Build') {
          steps {
                 echo "build final app"
                 sh 'mvn clean package'
          }
}
stage ('PROD') {
          steps {
                 echo "DEPLOY MY FINAL CODE TO PROD"
                 archiveArtifacts artifacts: 'java -jar my-app-1.0-SNAPSHOT.jar', followSymlinks: false
          }
}
}
}