 pipeline {
	agent any
	stages {
		stage ('build') {
			steps {
				sh "echo Building"
				nexusArtifactUploader(
				    nexusVersion: 'nexus3',
				    protocol: 'http',
				    nexusUrl: '192.168.43.76:8081',
				    groupId: 'com.github.jitpack',
				    version: '1.5-SNAPSHOT',
				    repository: 'maven-snapshots',
				    credentialsId: '3',
				    artifacts: [
					[artifactId: 'maven-simple',
					 classifier: 'maven-simple',
					 file: 'target/maven-simple-1.3.jar',
					 type: 'jar']
				    ]
				 )
				}
			}

		
		}

	}

