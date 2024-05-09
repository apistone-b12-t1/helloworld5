pipeline {
    agent any
    stages {
	stage('publish to exchange aabilash3') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint4') 
      }
      steps {
        bat 'mvn deploy -Duser="%ANYPOINT_CREDENTIALS_USR%"  -Dpass="%ANYPOINT_CREDENTIALS_PSW%"'
      }
    }
	stage('deploy to cloudhub aabilash3'){
	
environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint4') 
      }
      steps {
        bat 'mvn deploy  -DmuleDeploy  -Duser="%ANYPOINT_CREDENTIALS_USR%"  -Dpass="%ANYPOINT_CREDENTIALS_PSW%" -Denv="dev"'
      }
    }

	
}
}