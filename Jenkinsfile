pipeline {
  agent any
  tools {gradle 'Gradle'}
  stages {
    stage('SCM') {
      agent any
      steps {
        git(url: 'git@github.com:fredywang/SmartSpeaker.git', credentialsId: 'GitLab-SSH-KEY', branch: 'master')
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
