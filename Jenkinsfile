pipeline {
    agent any
    stages {
	stage('Deploy ARM') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint') 
      }
      steps {
        mvn deploy -Duser=${ANYPOINT_CREDENTIALS_USR}  -Dpass=${ANYPOINT_CREDENTIALS_PSW} 
      }
       

    }
}
}