node {
	checkout scm
	stage('Build') {
		sh 'make all'
		REPORT_CONTENT = sh('xsltproc check_unittest.xslt check-report.xml', returnStdout: true)
		echo $REPORT_CONTENT
		echo $REPORT_CONTENT > ./junit-report.html
	}

	stage('Report') {
		junit 'junit-report.html'
//		step([$class: "TapPublisher", testResults: "tap-report*.txt"])		
	}
}
