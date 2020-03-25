node {
	checkout scm
	def changeLog = tm('$GITCHANGELOG')
	echo changeLog
	stage('Build') {
		sh 'make all'
		sh 'xsltproc XML_for_JUnit.xsl check-report.xml > junit-report.xml'
	}

	stage('Report') {
		junit 'junit-report.xml'
		cobertura coberturaReportFile: 'coverage.xml', onlyStable: false
	}
}
