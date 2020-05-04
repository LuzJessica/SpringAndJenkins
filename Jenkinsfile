pipeline {
    agent
	{ 
		docker 
			{
			image 'maven:3.3.3' 
			image 'NodeJS 9.10.1'
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
		 stage('test')
		 {
            steps {
                sh 'npm install'
                sh 'npm run newman-tests'
                junit 'newman.xml'
            }
		}
	}
	     post 
		 {
        always 
		{
		        archiveArtifacts artifacts: 'target/helloworld-0.0.1-SNAPSHOT.war', onlyIfSuccessful: true
		}
	}
}	
