pipeline{
  agent none
	stages{
		stage('Build'){
		    steps{
		     sh 'ant -f PipelineAntbuild/build.xml'
		  }
		 }
		stage('Test'){
			steps{
			junit allowEmptyResults: true, testResults: 'PipelineAntbuild/build/test-reports/*.xml'
			}
		} 
	}
}