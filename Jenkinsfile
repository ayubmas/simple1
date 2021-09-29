
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				final String repo = env.GIT_URL.replaceFirst(/^.*\/([^\/]+?).git$/, '$1')
				final String user = "amassalha:1182626fa7f66f2e71672923dc955dce45"
				final String params = "token=1234&BUILD_TYPE=${repo}"
				final String url = "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/buildWithParameters?" + "${params}" 
				sh "which curl"
				final String response = sh(script: "/usr/bin/curl -I -k -vv -X POST -u ${user} ${url}", returnStdout: true).trim()
				echo response
			}
		}
				    
          }
    }
}
