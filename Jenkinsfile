node {
	checkout scm
	withDockerContainer(args: '-p 3000:3000', image: 'node:16-buster-slim') {
		stage('Build') {
			sh 'npm install'
		}
		stage('Test') {
			echo 'Test stage'
			sh './jenkins/scripts/test.sh'
		}
	}
}

