pipeline {
	agent {
		docker {
			image 'ghcr.io/jenkins-docs/quickstart-tutorials/jenkinsci-tutorials'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'composer install'
			}
		}
		stage('Test') {
			steps {
                sh './vendor/bin/phpunit tests'
            }
		}
	}
}