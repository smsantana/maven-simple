pipeline {
	agent any
	stages {
		stage ('build') {
			steps {
				sh "echo Building"
			}
		}

		stage ('uploadNexus') {
			nexusArtifactUploader artifacts: [
   				[artifactId: 'maven-simple', classifier: 'debug', file: 'target/maven-simple-1.3.jar', type: 'jar']], 
			credentialsId: '3', 
			groupId: 'com.github.jitpack', 
			nexusUrl: '192.168.43.76:8081', 
			nexusVersion: 'nexus3', 
			protocol: 'http', 
			repository: 'maven-snapshots', 
			version: '1.5-SNAPSHOT'
		}
		
		}

	}
