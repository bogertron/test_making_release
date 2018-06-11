pipeline {
	agent {
		node {
			label 'Master'
		}
	}

	stages {
		stage ('Build') {
			steps {
				bat "\"${tool 'VS2015_MSBuild'}\" Build.Proj /t:Build"
			}
		}
		
		stage ('Test') {
			steps {
				bat "echo running tests"
			}
		}
	}
}