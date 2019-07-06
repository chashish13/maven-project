pipeline {
    agent any
        stages {
            stage('Clone'){
                git 'https://github.com/chashish13/maven-project.git'
                }
            stage ('compile'){
                steps {
                    withMaven(maven : 'MVN_HOME')
                        sh 'mvn compile'
                        }
                 }
             }
         }
     }
                  
       
