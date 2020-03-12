pipeline {
	agent any
	stages {
		stage('First') {
			steps {
				script {
					env.EXECUTE="True"
				}
				sh 'echo "Step One"'
			}
		}
		stage('Second') {
		when {
			environment name: 'EXECUTE', value: 'True'
                } 
			steps {
				echo "Updating Second Stage"
				sh 'echo "Step two"'
			}			
		}
		stage('Third') {
		when {
			environment name: 'EXECUTE', value: 'False'
		}
			steps {
				sh 'echo "Step Three"'
			}		
		}
	}
} 
