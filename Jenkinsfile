pipeline {
   agent { label 'Maven' }
   environment {

        EMAIL_RECIPIENTS = 'bharathkumart5242@gmail.com'
   }
  stages {
    stage('checkout git'){
      steps {
    git credentialsId: 'jenkins1=bharath', url: 'https://github.com/bharath981/java-web.git'}
    }
    stage('Build'){
      steps {
        sh 'mvn clean install'
   }
       stage('unit testing'){
          steps {
          junit 'target/surefire-reports/*.xml'
          }
       }
    }
  }
}
  
