pipeline {
	agent {
		node {
			label 'Master'
		}
	}

	stages {
		stage ('Build') {
			steps {
				bat "\"${tool 'MSBuild'}\" Build.Proj /t:Build"
			}
		}
		
		stage ('Test') {
			steps {
				bat "echo running tests"
			}
		}
	}
}