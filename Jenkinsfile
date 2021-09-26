
pipeline {
    agent any

    stages {
        stage('Hello') {
            triggerRemoteJob job: "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/build?token=1234", 
				    parameters: "BUILD_TYPE=HEALTH")
				    
          }
    }
}
