
		
	    
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
        stage ('deploy') {
            steps {
                script {
                s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'warfiles123', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: '**', storageClass: 'STANDARD', uploadFromSlave: true, useServerSideEncryption: false]], pluginFailureResultConstraint: 'SUCCESS', profileName: 's3bucket', userMetadata: []
            }
        }
        
              
        }
    
    }
}
		
		
