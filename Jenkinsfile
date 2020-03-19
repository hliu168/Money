node {
	checkout scm
	stage('Build') {
		sh 'make all'
		sh 'xsltproc -o junit-report.xml check_unittest.xslt check-report.xml'
	}

	stage('Report') {
		junit 'junit-report.xml'
//		step([$class: "TapPublisher", testResults: "tap-report*.txt"])		
	}
}
