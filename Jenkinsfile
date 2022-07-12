pipeline {
    agent any
    environment {
        CUSTOM_ARGS ="--junitxml=junit.xml"

    }
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

