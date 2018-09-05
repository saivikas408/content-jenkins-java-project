pipeline {
  
  agent any
  
  stages {
    stage ('Build') {
      steps {
        sh 'ant -f build.xml -v'
        sh '${env.BUILD_NUMBER}'
      }
    }
    stage ('Deploy'){
      steps {
      sh 'cp /var/lib/jenkins/workspace/JAVA_PIPELINE/dist/*  /var/www/html' 
      }
    }
 }
}
