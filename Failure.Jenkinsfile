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
      junit '**/target/*.xml'
    }
    failure {
      mail to: "team.example.com", subject: 'The Pipeline filed :('
    }
  }
}