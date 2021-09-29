
pipeline {
    
    agent any

    stages {
        stage('Hello') {
		steps {
			script {
				final String repo = env.GIT_URL.replaceFirst(/^.*\/([^\/]+?).git$/, '$1')
				final String user = "amassalha:1182626fa7f66f2e71672923dc955dce45"
				final String params = '{"parameter": [{"name":"token", "value":"1234"}, {"name":"BUILD_TYPE", "value":"${repo}"}]}'
				final String url = "http://jenkins.beyondminds.ai:8080/job/Ayub/job/BUILD/buildWithParameters"
				sh "which curl"
				final String response = sh(script: "/usr/bin/curl -I -k -vv -X POST -u ${user} --data-urlencode json='${params}' ${url}", returnStdout: true).trim()
				echo response
			}
		}
				    
          }
    }
}
