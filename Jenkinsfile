pipeline {
    agent any
    tools {
	maven 'maven'
	jdk = 'JDK_8'	
		}
    stages {
        stage('build') {
            steps {
                sh 'mvn clean install'
                sh 'mvn spring-boot:run'
            }
        }
    }
}
