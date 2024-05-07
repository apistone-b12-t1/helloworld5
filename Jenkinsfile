pipeline {
    agent any
    stages {
	stage('Deploy ARM') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint') 
      }
      steps {
        bat 'mvn deploy -Duser="%ANYPOINT_CREDENTIALS_USR%"  -Dpass="%ANYPOINT_CREDENTIALS_PSW%"'
      }
    }
	stage('deploy to cloudhub'){
	
environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint') 
      }
      steps {
        bat 'mvn deploy  -DmuleDeploy  -Duser="%ANYPOINT_CREDENTIALS_USR%"  -Dpass="%ANYPOINT_CREDENTIALS_PSW%"'
      }
    }

}
}