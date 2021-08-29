pipeline {
    agent any

    environment {

    }

    tools {
        nodejs 'Jenkins-Node'
    }

    stages {

        stage('Initialize') {
            steps {
	    	git 'https://github.com/Yash-911/calculator.git'
                sh '''
                    npm install
                '''
            }
        }

        stage('Testing') {
            steps {
                sh '''
                    npm run test -- --watchAll=false
                '''
            }
        }

        stage('Build') {
            steps {
                sh '''
                    npm run build
                '''
            }
        }
    }
}
