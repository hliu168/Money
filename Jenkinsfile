node {
	checkout scm
	stage('Build') {
		sh 'make all'
	}

	stage('Report') {
		step([$class: "TapPublisher", testResults: "tap-report.txt"])		
	}
}
