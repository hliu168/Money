node {
	checkout scm
	stage('Build') {
		sh 'make all'
	}

	stage('Report') {
		junit 'coverage*.xml'
	}
}
