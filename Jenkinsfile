pipeline {
	agent any
	stages {

    	stage('Build Image') {
			steps {
			
            	withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'dockerhub', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD']]){
					sh '''
						docker build -t minageorge/udacity-devops-capstone .
					'''
				}

			}
		}

    }
}