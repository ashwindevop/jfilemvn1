pipeline {
     agent any
     
     tools {
         maven "jenkin-maven"
     }
     
     stages {
         
         stage('build') {
         
         steps {
              git 'https://github.com/ashwindevop/jar-28sep24.git'
              sh ' mvn clean package'
              sh ' scp /var/lib/jenkins/workspace/pipe10/target/vlc2.war 192.168.10.32:/opt/apache-tomcat-9/webapps/vlc2.war  '
         }
         }
     }
}

