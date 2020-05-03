pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
		sh 'mvn clean install'
            }
	stage('download'){
	    steps {
		sh 'echo "artifact file" > helloworld-0.0.1-SNAPSHOT.war'
	   }
    }
}
