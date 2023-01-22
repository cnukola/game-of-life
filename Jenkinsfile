node('JDK8') {
	stage('SourceCode') {
		git branch: 'sprint1-develop', url: 'https://github.com/cnukola/game-of-life.git'
}
	stage('BuildSteps') {
		sh 'mvn clean package'
}
     	stage('Archiving and Test Resuklts') {
		junit '**/surefile-reports/*.xml'
		archiveArtifacts artifacts: '**/*.war', followSymlinks: false
}
}
