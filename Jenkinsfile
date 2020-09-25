pipeline {
  agent {
    docker {
      image 'fredywang/jenkins_build:latest'
    }

  }
  stages {
    stage('SCM') {
      steps {
        git(url: 'git@github.com:fredywang/SmartSpeaker.git', credentialsId: 'GitLab-SSH-KEY', branch: 'master')
      }
    }

    stage('Build') {
      steps {
        sh 'gradle clean build'
      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }

    stage('test') {
      steps {
        sh 'echo test'
      }
    }

  }
}