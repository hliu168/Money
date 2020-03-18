node {

	stage('Build') {
		sh 'make all'
	}

	stage('Report') {
		junit './coverage.xml'
	}
}
