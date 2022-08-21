pipeline {
  agent any
  stages {
    stage('Test'){
      steps {
        sh 'echo Hello this is Failure Example!'
      }
    }
  }
  post{
    always {
      sh 'echo $?'
    }
    failure {
      sh "echo Failure Occured"
      sh "exit 1"
    }
  }
}