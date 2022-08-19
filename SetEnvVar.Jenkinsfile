pipeline {
  agent any 
  environment {
    userName = "CodingBUG"
  }
  stages {
    stage("Example for Environment Variable SetUP"){
      environment {
        DEBUG_FLAG = "-g"
      }
      steps {
        sh 'printenv'
      }
    }
  }
}