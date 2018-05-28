pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Automated-operation') {
          git(url: 'git@github.com:poetL/Automated-operation.git', branch: 'master', credentialsId: ' 9850ca09563a0f2fc34d0be0ff7e28465469128f')
        }

      }
    }
  }
}