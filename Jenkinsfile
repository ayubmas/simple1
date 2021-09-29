
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				def repo = env.GIT_URL.replaceFirst(/^.*\/([^\/]+?).git$/, '$1')
				def handle = triggerRemoteJob job: 'http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/', 
					parameters: "BUILD_TYPE=${repo}", token: '1234', useCrumbCache: true, useJobInfoCache: true

				echo 'Remote Status: ' + handle.getBuildStatus().toString()
			}
		}
				    
          }
    }
}
