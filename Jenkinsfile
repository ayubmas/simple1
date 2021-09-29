
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				def repo = env.GIT_URL.replaceFirst(/^.*\/([^\/]+?).git$/, '$1')
				def handle = triggerRemoteJob( job: "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/JobWithParams?token=1234&BUILD_TYPE=$repo",
						 parameters:"BUILD_TYPE=${repo}",
						 token: '1234', blockBuildUntilComplete: true)
				echo 'Remote Status: ' + handle.getBuildStatus().toString()
			}
		}
				    
          }
    }
}
