pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/poet1/Automated-operation.git') {
          git(url: 'git@github.com:poetL/Automated-operation.git', branch: 'master', credentialsId: 'dfb23854d8ce174320daec944663649659ec979f')
        }

      }
    }
    stage('build') {
      steps {
        sh 'sudo pip -r requirements.txt '
      }
    }
    stage('run') {
      steps {
        sh 'python app.py'
      }
    }
  }
}