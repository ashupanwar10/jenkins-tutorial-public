def timeInMillis = currentBuild.timeInMillis
def imageTag = "initkloud/alpine:" + timeInMillis

@Library("shaed-library") _
pipeline {
  agent any
  environment {
    DH_CREDS = credentials('dh-creds')
  }
  stages {
    stage("Hello"){
      steps {
        sh """
          echo "FROM alpine:latest > Dockerfile"
          docker build -t ${imageTag}
        """
        sh '''
          echo $DH_CREDS_PSD | docker login --username=$DH_CREDS_USR --password-stdin
        '''
        script {
          def sha256 = sh(returnStdout: true, script: "docker push ${imageTag} | grep sha256 | awk -F':' '{print \$1}'").trim()
          echo sha256
          def url = "https://hub.docker.com/layers/" + env.DH_CREDS_USR + "/alpine/" + timeInMillis + "/images/sha256-" + sha256 + "?context=explore"
          addSidebarLink(url:url,text:"Image on Docker Hub",icon:"star.gif")
        }
      }
      post {
        always {
          sh 'docker logout'
        }
      }
    }
  }
}