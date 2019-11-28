pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git(url: 'https://github.com/Rajendra333/app.git', branch: 'master')
      }
    }
    stage('deploy') {
      steps {
       
         bat ' \'del "C:\\\\Program Files\\\\Apache Software Foundation\\\\Tomcat 8.5\\\\webapps\\\\gamutkart.war	 " && xcopy "C:\\\\Program Files (x86)\\\\Jenkins\\\\workspace\\\\app\\\\target\\\\gamutkart.war" "C:\\\\Program Files\\\\Apache Software Foundation\\\\Tomcat 8.5\\\\webapps"\''

      }
    }
  }
}
