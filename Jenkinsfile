// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// }

pipeline {
    agent any
    // agent { docker { image "maven:3.6.3" } }
    environment {
        dockerHome = tool 'myDocker'
        mavenHome = tool 'myMaven'
        PATH = "$dockerHone/bin:$mavenHome/bin:$Path"
    }

    stages {
        stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
        stage('integration test') {
            steps {
                sh "mvn failsafe:integration-test failsafe:verify"
            }
        }
    }
    // stages {
    //     stage('Build') {
    //         steps {
    //             sh 'mvn --version'
    //             echo "Build"
    //         }
    //     }
	// stage('Test') {
    //         steps {
    //             echo "Test"
    //         }
    //     }
    // }

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