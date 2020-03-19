node {
	checkout scm
	stage('Build') {
		sh 'make all'
		sh 'xsltproc check_unittest.xslt check-report.xml > junit-report.html'
	}

	stage('Report') {
		junit 'junit-report.html'
//		step([$class: "TapPublisher", testResults: "tap-report*.txt"])		
	}
}
