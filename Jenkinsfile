pipeline{
  agent any
	stages{
		stage('Build'){
		    steps{
		     sh 'ant -f PipelineAntbuild@script/build.xml'
		  }
		 }
		stage('Test'){
			steps{
			junit allowEmptyResults: true, testResults: 'PipelineAntbuild@script/build/test-reports/*.xml'
			}
		} 
	}
}