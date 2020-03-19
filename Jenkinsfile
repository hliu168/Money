node {
	checkout scm
	stage('Build') {
		sh 'make all'
	}

	stage('Report') {
		junit 'junit-report.xml'
		
	}
}
