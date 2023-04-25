pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scmGit(
        branches: [[name: 'main']],
        userRemoteConfigs: [[url: 'https://github.com/Marshmillo/3d-portfolio.git']])
      }
    }
    stage('Install Dependencies') {
      steps {
        nodejs('nodejs-14.17.0') {
          sh 'npm install'
        }
      }
    }
    stage('Build') {
      steps {
        nodejs('nodejs-14.17.0') {
          sh 'npm run build'
        }
      }
    }
    stage('Deploy') {
      steps {
        sh 'ls -l'
      }
    }
  }
}