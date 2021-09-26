
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				
				def repo = env.GIT_URL.replaceFirst(/^.*\/([^\/]+?).git$/, '$1')
				triggerRemoteJob job: "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/build", 
					parameters: "BUILD_TYPE=${repo}"
			}
		}
				    
          }
    }
}
