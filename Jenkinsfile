pipeline {
	agent any
	tools { 
	         maven 'Maven_Local' 
                 jdk 'Jdk_Localhost' 
      }
	stages {
		stage('---clean---'){
			steps {
				
				 bat "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				
				bat "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'Maven_Local', type: 'maven'
				bat "mvn package"
			}
		}
		
		stage('---deploy to tomcat---'){
			steps {
				bat("xcopy C:\Program Files (x86)\Jenkins\workspace\Pipeline-maven\target\jenkins-example-1.0-SNAPSHOT.jar C:\Program Files\Apache Software Foundation\Tomcat 8.5\webapps")
			}
		}
		
		
	}
}
