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
 		when {
			environment name: 'EXECUTE', value: 'True'
                }
		stage('Second') { 
			steps {
				echo "Updating Second Stage"
				sh 'echo "Step two"'
			}			
		}
		stage('Third') {
			steps {
				sh 'echo "Step Three"'
			}		
		}
	}
} 
