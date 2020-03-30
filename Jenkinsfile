pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
	stage('build'){
	    steps{
		retry(3){
		    sh 'echo "hello World!'
	    	    sh 'python --version'
	    	}
	    timeout(time: 3, unit: 'MINUTES'){
		sh 'echo "healthcheck needs to be done"'
	    	}
	    }
    	}
    }		     
}


