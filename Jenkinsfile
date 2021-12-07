pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        echo 'this is the first job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the second job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the third job'
        sh 'npm run package'
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}