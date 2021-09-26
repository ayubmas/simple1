
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
				def handle = triggerRemoteJob job: "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/build", 
					parameters: "BUILD_TYPE=$env.GITHUB_REPOSITORY"
			}
				    
          }
    }
}
