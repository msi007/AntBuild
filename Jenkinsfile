pipeline{
  agent none
	stages{
		stage('Build'){
			agent {label 'master'}
		    steps{
			withAnt(installation: 'Ant_1.10.12', jdk: 'jdk1.8.0_161') {
    // some block

		     sh 'ant -f build.xml'
		  }
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