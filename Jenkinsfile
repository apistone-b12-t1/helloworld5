pipeline {
    agent any
    stages {
	stage('publish to exchange aabilash4') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint') 
      }
      steps {
        bat 'mvn deploy -Duser="%ANYPOINT_CREDENTIALS_USR%"  -Dpass="%ANYPOINT_CREDENTIALS_PSW%"'
      }
    }
	stage('deploy to cloudhub aabilash4'){
	
environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint') 
      }
      steps {
        bat 'mvn deploy  -DmuleDeploy  -Duser="%ANYPOINT_CREDENTIALS_USR%"  -Dpass="%ANYPOINT_CREDENTIALS_PSW%"'
      }
    }

	
}
}