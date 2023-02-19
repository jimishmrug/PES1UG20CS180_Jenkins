pipeline {
	    agent any
	

	    stages {
	        stage('Build') {
	            steps {
	                sh 'g++ -o hello a.cpp'
                  build job: 'PES1UG20CS180-1'
                  echo "Build Successful"
	            }
	        }
	

	        stage('Test') {
	            steps {
	                sh './hello'
                  echo "Test Successful"
	            }
	        }
	

	        stage('Deploy') {
	            steps {
                  sh ' echo "Deployment stage"'
                  sh 'exit 1'
	                echo 'Deploy successfull'
	            }
	        }
	    }
	

	    post {
	        always {
	            script {
	                if (currentBuild.result == 'FAILURE') {
	                    echo 'pipeline failed'
	                }
	            }
	        }
	}
}
