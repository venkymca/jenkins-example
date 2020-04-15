pipeline {
	agent any
	stages {
		stage('---clean---'){
			steps {
				tool name: 'Maven_Local', type: 'maven'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'Maven_Local', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'Maven_Local', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
