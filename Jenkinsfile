pipeline {
	agent any
	stages {
		stage('First') {
			steps {
				script {
					env.EXECUTE="False"
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
			steps {
				sh 'echo "Step Three"'
			}		
		}
	}
} 
