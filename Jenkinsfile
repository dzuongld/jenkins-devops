// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// }

pipeline {
    //agent any
    agent { docker { image: "maven:3.6.3" } }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                echo "Build"
            }
        }
	stage('Test') {
            steps {
                echo "Test"
            }
        }
    }

    post {
        always {
            echo "all the time"
        }
        success {
            echo "success"
        }
        failure {
            echo "failure"
        }
    }
}