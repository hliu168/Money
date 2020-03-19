node {
	checkout scm
	stage('Build') {
		sh 'make all'
		sh 'xsltproc XML_for_JUnit.xsl check-report.xml > junit-report.xml'
	}

	stage('Report') {
		junit 'junit-report.xml'
//		step([$class: "TapPublisher", testResults: "tap-report*.txt"])		
	}
}
