
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				
				def repo = env.GITHUB_REPOSITORY
				triggerRemoteJob job: "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/build", 
					parameters: "BUILD_TYPE=${repo}"
			}
		}
				    
          }
    }
}
