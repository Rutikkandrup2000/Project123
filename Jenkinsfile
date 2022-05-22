pipeline{
  agent any
  stages{
    stage('git repo & clean'){
      steps{
        bat " rmdir /s /q employee"
        bat "git clone https://github.com/hakamaru/employee.git"
        
      }
    }
    stage('install'){
      steps{
        bat "mvn install -f employee"
      }
    }
    stage('test'){
      steps{
        bat "mvn test -f employee"
      }
    }
    stage('package'){
      steps{
        bat "mvn package -f employee"
      }
    }
  }
}
