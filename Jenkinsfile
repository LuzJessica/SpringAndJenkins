pipeline {
    agent { docker { image 'maven:3.5.3' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean install'
                sh 'mvn spring-boot:run'
            }
        }
    }
}
