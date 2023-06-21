pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'this is the build  the app job'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'this is the test the app job'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'this is the package the app job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this the first pipeline developed through code has completed...'
    }

  }
}