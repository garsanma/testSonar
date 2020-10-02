def server_up = false

pipeline {
//agent any
    agent { label "sdk5" }
  
	 stage('Sonarqube') {
    		environment {
        	scannerHome = tool 'SonarQubeScanner'
    		}
   	    steps {
       		 withSonarQubeEnv('SonarQubeGarsanma') {
           	 sh "${scannerHome}/bin/sonar-scanner -X -Dsonar.java.binaries=. -Dsonar.projectKey=my-project-garsanma -Dsonar.sources=."
       	    	}
           }
   	 }

    }
}  
