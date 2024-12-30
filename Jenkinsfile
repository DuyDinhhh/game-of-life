node('JDK8'){
	stage('Sourcecode'){
		git config --global http.version HTTP/1.1 
		git branch: 'sprint1-develop', url: 'https://github.com/DuyDinhhh/game-of-life.git'
	}
	stage('Build the code'){
		sh 'mvn clean package'
	}
	stage('Archiving and Test Results'){
		junit '**/surefire-reports/*.xml'
		archiveArtifacts artifacts: '**/*.war', followSymlinks: false
	}
}

