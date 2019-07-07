pipeline {
    agent any


    stages {
        stage('SCM Checkout'){
          git 'https://github.com/chashish13/maven-project.git'
        }
  }
    {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MVN_HOME') {
                    sh 'mvn clean compile'
                }
            }
        }            
}
            {
        stage ('Install Stage') {

            steps {
                withMaven(maven : 'MVN_HOME') {
                    sshagent (credentials: ['cc425ba9-fa91-4557-92ae-82c130abdb3a']) {
                       sh 'scp -o StrictHostKeyChecking=no -l ec2-ser@172.31.46.121:/var/lib/tomcat/'

                }
            }
}
}
}
