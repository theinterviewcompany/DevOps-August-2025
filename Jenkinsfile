pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          if (env.BRANCH_NAME == 'main') {
            echo "Building MAIN branch"
          } else if (env.BRANCH_NAME == 'develop') {
            echo "Building DEVELOP branch"
          } else {
            echo "Skipping unsupported branch: ${env.BRANCH_NAME}"
            currentBuild.result = 'SUCCESS'
            return
          }
        }
      }
    }
  }
}
