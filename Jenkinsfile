node {
	checkout scm
	stage('Build') {
//		sh 'make all'
//		sh 'cat tap-report.txt | tap-xunit > junit-report.xml'
	}

	stage('Report') {
		junit 'junit-report.html'
//		step([$class: "TapPublisher", testResults: "tap-report*.txt"])		
	}
}
