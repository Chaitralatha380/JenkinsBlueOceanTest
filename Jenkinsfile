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
        sh 'mvn -f simple-java-maven-app-master/pom.xml compile'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn -f simple-java-maven-app-master/pom.xml test'
      }
    }

  }
}