pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git(url: 'https://github.com/nehasri17/github-maven-example.git', branch: 'master', credentialsId: 'nehasri17', changelog: true, poll: true)
        echo 'hello world'
      }
    }
    stage('build') {
      steps {
        sh 'mvn test'
      }
    }
    stage('print massage') {
      steps {
        sh 'echo "hello world"'
      }
    }
  }
}