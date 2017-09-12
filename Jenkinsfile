pipeline {
	agent any
	stages {
		stage ('build') {
			steps {
				sh "echo Building"
			}
		}

		stage ('uploadNexus') {
			nexusArtifactUploader artifacts: [[artifactId: 'com.github.jitpack', classifier: 'maven-simple', file: 'target/maven-simple-1.3.jar', type: 'jar']], credentialsId: '3', groupId: 'com.github.jitpack', nexusUrl: '192.168.43.76:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'com.github.jitpack', version: '2.0'
		}
		
		}

	}
