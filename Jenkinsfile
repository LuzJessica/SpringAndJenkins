pipeline {
    agent
	{ 
		docker 
			{
			image 'maven:3.3.3' 
			}	 
	}
    stages 
	{
        stage('build') 
		{
            steps 
			{
                sh 'mvn --version'
				sh 'mvn clean install'
            }
		}
	}
	     post 
		 {
        always 
		{
		        archiveArtifacts artifacts: './target/helloworld-0.0.1-SNAPSHOT.war', onlyIfSuccessful: true
		}
	}
}	
