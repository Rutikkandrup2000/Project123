pipeline{
  agent any
  stages{
    stage('git repo & clean'){
      steps{
        bat " rmdir /s /q employee"
        bat "git clone https://github.com/hakamaru/employee.git"
        bat " clean -f employee"
      }
    }
    stage('install'){
      steps{
        bat " install -f employee"
      }
    }
    stage('test'){
      steps{
        bat " test -f employee"
      }
    }
    stage('package'){
      steps{
        bat " package -f employee"
      }
    }
  }
}
