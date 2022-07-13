pipeline {
    agent any
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