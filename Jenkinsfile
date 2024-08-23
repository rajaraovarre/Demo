pipeline {
    agent any

environment{

   PATH="${PATH}:/opt/maven/bin"
}

    stages {
        stage('CLONE') {
            steps {
                git branch: 'main', credentialsId: 'Github-Login', url: 'https://github.com/rajaraovarre/Demo.git'
            }
        }
        stage('BUILD') {
            steps {
                sh "mvn clean package"
            }
        }
        
    }
}

