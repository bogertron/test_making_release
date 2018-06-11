pipeline {
	agent {
		node {
			label 'Master'
		}
	}

	stages {
		stage ('Build') {
			bat "\"${tool 'MSBuild'}\" Build.Proj /t:Build"
		}
		
		stage ('Test') {
			bat "echo running tests"
		}
	}
}