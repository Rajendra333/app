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
    stage('Sonar') {
      steps {
        bat 'mvn sonar:sonar'
      }
    }
    stage('Notification') {
      steps {
        mail(subject: 'test', body: 'application sucess', to: 'rajendra.r2t@gmail.com', from: 'rajendrachowdary40@gmail.com')
      }
    }
    stage('Deploy') {
      steps {
        bat 'bat \'del "C:\\\\Program Files\\\\Apache Software Foundation\\\\Tomcat 8.5\\\\webapps\\\\gamutkart.war	 " && xcopy "C:\\\\Program Files (x86)\\\\Jenkins\\\\workspace\\\\madhuapp_master\\\\target\\\\gamutkart.war" "C:\\\\Program Files\\\\Apache Software Foundation\\\\Tomcat 8.5\\\\webapps"\''
      }
    }
  }
}