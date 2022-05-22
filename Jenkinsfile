pipeline{
    agent any
    tools{
      maven 'MAVEN'
    
    
   }   
   stages{
       
       stage("Maven Build"){
           steps{
               sh 'mvn -Dmaven.test.failure.ignore=true clean package'
           
           }
       }
   }
}
