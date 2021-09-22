
pipeline {
    agent any

    stages {
        stage('Hello') {
            build job: "BUILD", 
				    parameters: [
					    string(name: "BUILD_TYPE", value: "HEALTH")
				    ]
          }
    }
}
