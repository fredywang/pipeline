pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git(url: 'https://github.com/fredywang/SmartSpeaker.git', branch: '*/master')
      }
    }

    stage('Build') {
      steps {
        sh 'gradle clean build'
      }
    }

    stage('Deploy') {
      steps {
        echo '......Deploy....'
      }
    }

    stage('SmokeTest') {
      steps {
        echo 'SmokeTest'
      }
    }

  }
}