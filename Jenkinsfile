
		
	    
pipeline {
    agent any 
    stages {
        stage('Checkout') { 
            steps {
                script {
                 git 'https://github.com/cjpcloud/warrepo.git'

            }
        }
        }
        stage('Build') { 
            steps {
                script {
                sh 'mvn clean package'
            }
        }
        
        }
    
    }
}
		
		
