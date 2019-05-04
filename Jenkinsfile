pipeline {
    agent any
    stages {
        stage('pre-check') {
            steps {
                sh 'mvn --version'
            }
        }
	stage('Build') {
            steps {
                echo 'Building..'
		sh 'mvn clean compile package'
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
		sh 'java -jar ./target/*.jar'
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
