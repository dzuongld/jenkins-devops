// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// }

pipeline {
    stages {
        stage('Build') {
            steps {
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