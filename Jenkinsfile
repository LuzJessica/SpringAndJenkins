pipeline {
    agent { docker { image 'jenkins/jenkins' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean install'
                sh 'mvn spring-boot:run'
            }
        }
    }
}
