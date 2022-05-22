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
        bat 'MAVEN install -f employee'
      }
    }
    stage('test'){
      steps{
        bat 'MAVEN test -f employee'
      }
    }
    stage('package'){
      steps{
        bat 'MAVEN package -f employee'
      }
    }
  }
}
