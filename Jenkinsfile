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
    post {
        always {
            echo 'One way or another, I have finished'
            /* deleteDir() clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
