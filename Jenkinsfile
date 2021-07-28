pipeline {
  agent any
  environment {
    COURSE = 'DevOps Practice'
    BRANCH = 'main'
  }
  stages {
    stage('Audit Tools') {
      steps {
        echo "Audit all the tools to use in this pipeline ${BRANCH}"
        sh "git --version"
        sh "node --version"
        sh "npm --version"
        sh "ng --version"
        sh "ansible --version"
        echo "Workspace folder: ${WORKSPACE}"
      }
    }
    stage('Install Packages') {
      steps {
        dir("{$WORKSPACE}/conduit-ui"){
          echo 'Install conduit UI packages'
          sh 'npm install'
        }
      }
    }
  }
}
