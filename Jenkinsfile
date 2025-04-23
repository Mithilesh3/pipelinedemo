pipeline {
  agent any
  stages {
    stage('fetch') {
      steps {
        git(url: 'https://github.com/Mithilesh3/pipelinedemo.git', branch: 'main', poll: true)
      }
    }

    stage('build') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}