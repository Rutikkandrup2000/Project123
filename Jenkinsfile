pipeline
{
   agent any
  
  stages
  {
    stages('Build')
    {
      steps
      {
        echo 'Build App'
      }
    }
    
    stage('Test')
    {
      steps
      {
        echo 'Test App'
      }
    }
    
    stage('Deploy')
    {
      steps
      {
        echo 'Deploy App'
      }
    }
  }
  
  post
  {
    
    always
    {
      emailext.body: .'Summary',.subject:.'Pipeline.Status',.to:.'chikunaik07@gmail.com'
    }
    
  }
}
