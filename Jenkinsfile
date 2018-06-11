pipeline {
	agent {
		node {
			label 'Master'
		}
	}
	parameters { 
		string(name: 'TESTSTR', defaultValue: 'Test', description: 'Can this be set')
	}

	stages {
		stage ('Build') {
			steps {
				bat "\"${tool 'VS2015_MSBuild'}\" Build.Proj /t:Build"
			}
		}
		
		stage ('Test') {
			steps {
				bat "echo running tests: ${params.TESTSTR}"
			}
		}
	}
}