
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				def repo = env.GIT_URL.replaceFirst(/^.*\/([^\/]+?).git$/, '$1')
				curl -x POST "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/buildWithParameters?token=1234&BUILD_TYPE=$repo"
			}
		}
				    
          }
    }
}
