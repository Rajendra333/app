pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git(url: 'https://github.com/Rajendra333/app.git', branch: 'master')
      }
    }
    stage('Build') {
      steps {
        bat 'mvn clean package'
      }
    }
    stage('Test') {
      steps {
        bat 'mvn test'
      }
    }
  }
}