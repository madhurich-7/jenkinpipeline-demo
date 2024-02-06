pipeline {
  agent any
  stages {
    stage('Install webserver') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('fetch code') {
      steps {
        git(url: 'https://github.com/madhurich-7/jenkinpipeline-demo.git', branch: 'main')
      }
    }

    stage('deploy code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}