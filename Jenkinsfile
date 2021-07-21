pipeline {
	agent none  
	stages {
		stage('BUILD') {
      		agent {label 'tag1'}
			steps {
				catcherror (buildResult: 'SUCCESS', stageResult: 'FAILURE') {
					echo "build"
					sh 'sleep 15'
					sh 'exit 1'
				}
			}	
		}
		stage('TEST') {
      		agent {label 'tag2'}
			steps {
					echo "test"
			}	
		}
		
	}
}
