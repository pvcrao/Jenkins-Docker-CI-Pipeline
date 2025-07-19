pipeline {
  agent any
  environment {
    DOCKER_HUB_CREDENTIALS = credentials('docker-hub-credentials')
    IMAGE_NAME = "yourdockerhubusername/jenkins-pipeline-app"
  }
  stages {
    stage('Clone Repo') {
      steps {
        git 'https://github.com/prashanthkumaryerra/jenkins-docker-ci-pipeline.git'
      }
    }
    stage('Build Docker Image') {
      steps {
        script {
          docker.build("${IMAGE_NAME}")
        }
      }
    }
    stage('Push to DockerHub') {
      steps {
        script {
          docker.withRegistry('', DOCKER_HUB_CREDENTIALS) {
            docker.image("${IMAGE_NAME}").push("latest")
          }
        }
      }
    }
    stage('Deploy (Optional)') {
      steps {
        echo 'Trigger remote deployment... (coming soon)'
      }
    }
  }
}
