pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/chashish13/maven-project.git'
        }
  }
    {
        stage ('Install Stage') {

            steps {
                withMaven(maven : 'MVN_HOME') {
                    sh 'mvn clean install'
                }
            }
        }
    }
{
stage ('scp Stage') {

steps {
sshagent (credentials: ['cc425ba9-fa91-4557-92ae-82c130abdb3a']) {
sh 'scp -o StrictHostKeyChecking=no webapp/target/*.war ec2-user@172.31.46.121:/var/lib/tomcat/webapps'


    }
}
}
}
}
