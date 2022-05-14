pipeline {

agent any

stages {
stage ('SCM') {
         steps {
                 echo "git pull my code"
                 git 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
         }
}
stage ('Build') {
          steps {
                 echo "build final app"
                 sh 'mvn clean package'
          }
}
stage ('Deploy') {
          steps {
                 echo "DEPLOY MY FINAL CODE TO PROD"
                 sh 'java -jar target/*.jar'
          }
}
}
}