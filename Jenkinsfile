pipeline {
    agent { docker { image 'python:3.7.2' } }
       stages {
        stage('Clone Repository') {
          steps {
            checkout scm
           }
        }
        stage('test ml_api') {
            steps {
                dir("packages/ml_api/") {
                sh "pip install tox"
                sh "tox "
                }
          }
		}
	   }
}