pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package --batch-mode'
                sh "docker build . -t tomcat_webapp:${env.BUILD_ID}"
            }
        }
    }
}
