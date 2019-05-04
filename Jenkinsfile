pipeline {
    agent any
    stages {
	stage('check-echo'){
	    echo '######### Echo check  #########'
	}
	stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('pre-check') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
