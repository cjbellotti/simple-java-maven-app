pipeline {
	agent {
		docker {
			image 'maven:3-alpine'
			args '-u root:sudo -v $HOME/.m2:/root/.m2 -v /var/run/docker.sock:/var/run/docker.sock'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn -B -DskipTests clean package'
			}
		}
	}
}
