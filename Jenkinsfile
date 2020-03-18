node {
	checkout scm
	stage('Build') {
		sh 'make all'
	}

	stage('Report') {
		cobertura coberturaReportFile: 'coverage.xml'
	}
}
