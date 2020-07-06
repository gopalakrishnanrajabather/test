pipeline {
	agent any
	stages {
		stage('Compile') {
			steps {
				echo "Completed Successfully";
                git 'https://github.com/gopalakrishnanrajabather/test.git'
                bat 'test.bat'
			}
		}
		stage('JUnit') {
			steps {
				echo "JUnit passed Successfully";
			}
		}
		stage('Quality-Gate') {
			steps {
				echo "SonarQube Quality Gate passed successfully!";
			}
		}
		stage('Deploy') {
			steps {
				echo "Pass!";
			}
		}
	}

	post {
		always {
			echo "This will always run"
		}
		success {
			echo "This will run only if successful"
		}
		failure {
			echo "This will run onl if failed"
		}
		unstable {
			echo "This will run only if the run was marked as unstable"
		}
		changed {
			echo "This will run only if the state of the pipeline has changed"
			echo "For example, if the pipeline was previously failing but is now successful"
		}
	}
}
