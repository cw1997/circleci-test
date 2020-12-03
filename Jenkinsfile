pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "hello world"'
      }
    }

    stage('deploy') {
      parallel {
        stage('deploy') {
          steps {
            echo 'deploy'
            sh 'echo \'build complete!\''
          }
        }

        stage('concurrent deploy') {
          steps {
            sh 'echo \'concurrent deploy / Shell Script\''
          }
        }

      }
    }

  }
}