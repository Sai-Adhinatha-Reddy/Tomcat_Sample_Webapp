pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'jar -cvf basic.war *'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp basic.war /tomcat/apache-tomcat-11.0.6/webapps/'
            }
        }
    }
	post {
			success {
				// Actions to perform on successful build
				echo 'Build and deployment successful!'
			}
			failure {
				// Actions to perform on build failure
				echo 'Build or deployment failed!'
			}
		}
}

