pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
				sh 'g++ ./pipeline/pes1ug20cs111_task5.cpp -o ./pipeline/pes1ug20cs111_task5'
				echo 'Build Stage Successful.'
				build job: 'PES1UG20CS111-1'
			}
		}
		stage('Test') {
			steps {
				sh './pes1ug20cs111_task5'
				echo 'Test Stage Successful.'
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deployment Successful.'
			}
		}
	}
	post {
		failure {
			echo 'Pipeline Failed.'
		}
	}
}
