pipeline {
    agent any
    stages {
	stage('Deploy ARM') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint') 
      }
      steps {
        sh 'mvn deploy -Duser=${ANYPOINT_CREDENTIALS_USR}  -Dpass=${ANYPOINT_CREDENTIALS_PSW}' 
      }
        stage ('Building') {
            steps { 
			
			
			
               // --bat 'mvn deploy --settings C:/Users/326078/.m2/settings.xml -DmuleDeploy ' 
            }            
        }

    }
}
}