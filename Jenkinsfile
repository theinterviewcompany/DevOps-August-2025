pipeline {
    agent any

    stages {
        stage('GIT checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/theinterviewcompany/java-maven-war-app.git']])
            }
        }
    }
}
