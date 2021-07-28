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
      }
    }
    stage('Install Packages') {
      steps {
        echo "Install conduit UI package"
        sh "npm install"
      }
    }
   
  }
  
}
