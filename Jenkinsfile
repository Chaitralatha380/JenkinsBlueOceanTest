pipeline {
  agent any
  stages {
    stage('CloneRepo') {
      steps {
        git(url: 'https://github.com/Chaitralatha380/MavenDemo.git', changelog: true, poll: true, branch: 'master')
      }
    }

    stage('Compile') {
      steps {
        sh '''mvn clean
mvn compile'''
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

  }
}