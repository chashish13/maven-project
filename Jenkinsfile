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
                    sh 'mvn install'
                }
            }
}
}
}
