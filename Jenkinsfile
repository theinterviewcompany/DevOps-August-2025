pipeline {
    agent any

    tools {
        maven 'Maven_3_9_7'
    }

    stages {
        stage('GIT checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/theinterviewcompany/java-maven-war-app.git']])
            }
        }
        stage('maven build') {
            steps {
                 sh 'mvn clean install'            }
        }
    }
}
