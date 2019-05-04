pipeline {
    agent any
    stages {
	stage('check-echo'){
	    echo '######### Echo check  #########'
	}
        stage('pre-check') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
