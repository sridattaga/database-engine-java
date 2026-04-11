pipeline {
 agent none
 stages {
     stage ('git checkout')
     {
         agent { label 'siva' }
         steps {
                 git branch: "${env.BRANCH_NAME}", 
                url: 'https://github.com/sridattaga/database-engine-java.git'
         }
     }
     stage ('validate the code')
     {
         agent { label 'siva' }
         steps{
             sh 'mvn validate'
         }
     }
     stage ('compile the code')
     {
         agent { label 'siva' }
       steps {
           sh 'mvn compile'
       } 
     }
     stage ('test the code')
     {
         agent { label 'siva' }
         steps {
             sh 'mvn test'
         }
     }
     stage ('package the code')
     {
         agent { label 'siva' }
         steps{
             sh 'mvn package'
         }
     }
 }
}
