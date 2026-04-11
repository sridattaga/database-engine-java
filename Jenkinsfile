pipeline {
 agent any
 stages {
     stage ('git checkout')
     {
         steps {
                checkout scm
         }
     }
     stage ('validate the code')
     {
        steps{
             sh 'mvn validate'
         }
     }
     stage ('compile the code')
     {
        steps {
           sh 'mvn compile'
       } 
     }
     stage ('test the code')
     {
         steps {
             sh 'mvn test'
         }
     }
     stage ('package the code')
     {
         steps{
             sh 'mvn package'
         }
     }
 }
}
