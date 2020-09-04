pipeline {
  agent any
  stages {
    stage('SCM') {
      agent any
      steps {
        git(url: 'https://github.com/fredywang/SmartSpeaker.git', credentialsId: 'GitLab-SSH-KEY', changelog: true)
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