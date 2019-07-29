pipeline {
    agent {
    	image 'node:6-alpine'
	args '-p 10005:3000 -p 10006:5000'
    }
    environment {
    	CI = 'true'
    }
    stages {
    	stage('Build'){
			steps{
				sh 'npm install'
			}
		}
		stage('Test'){
			steps{
				sh './jenkins/scripts/test.sh'
			}
		}
    }
}
