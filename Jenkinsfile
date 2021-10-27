pipeline{
  agent any
	stages{
		stage('Build'){
		    steps{
		     sh 'ant -f PipelineAntbuild@script/biuld.xml'
		  }
		 }
		stage('Test'){
			steps{
			junit allowEmptyResults: true, testResults: 'PipelineAntbuild@script/build/test-reports/*.xml'
			}
		} 
	}
}