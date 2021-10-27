pipeline{
  agent none
	stages{
		stage('Build'){
			agent {label 'master'}
		    steps{
		     sh 'ant -f PipelineAntbuild/build.xml'
		  }
		 }
		stage('Test'){
			agent {label 'master'}
			steps{
			junit allowEmptyResults: true, testResults: 'PipelineAntbuild/build/test-reports/*.xml'
			}
		} 
	}
}