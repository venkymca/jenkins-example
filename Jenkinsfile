pipeline {
	agent any
	stages {
		stage('---clean---'){
			steps {
				tool name: 'Maven_Local', type: 'maven'
				"mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'Maven_Local', type: 'maven'
				"mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'Maven_Local', type: 'maven'
				"mvn package"
			}
		}
	}
}
