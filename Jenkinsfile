#node('JDK8') {
#	stage('sourcecode') {
#		git branch: 'dev1', url: 'https://github.com/cnukola/game-of-life.git'
#	}
#	stage('Build the code') {
#		sh 'mvn clean package'
#	}
#	stage('Archiving and Test results') {
#		junit '**/surefire-reports/*.xml'
#		junit '**/surefire-reports/*.xml'
#	}
#}





pipeline {
	agent { label 'JDK8' }
	stages {
		stage('SourceCode') {
			steps {
				git branch: 'dev1', url: 'https://github.com/cnukola/game-of-life.git'
			}
		}
		stage('Build the code') {
			steps {
				sh 'mvn clean package'
			}
		}
		stage('Archiving and Test Results') {
			steps {
				junit '**/surefire-reports/*.xml'
				archiveArtifacts artifacts: '**/*.war', followSymlinks: false
			}
		}
	}
}
