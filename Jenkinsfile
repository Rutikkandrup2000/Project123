pipeline{
  agent any
  stages{
    stage('git repo & clean'){
      steps{
        bat "rmdir /s /q employee"
        bat "git clone https://github.com/hakamaru/employee.git"
        bat "maven clean -f employee"
      }
    }
    stage('install'){
      steps{
        bat "maven install -f employee"
      }
    }
    stage('test'){
      steps{
        bat "maven test -f employee"
      }
    }
    stage('package'){
      steps{
        bat "maven package -f employee"
      }
    }
  }
}
    
