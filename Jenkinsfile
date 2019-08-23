pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        openshiftBuild 'php-pipeline-test'
      }
    }
    stage('Verify build') {
      steps {
        openshiftVerifyBuild 'php-pipeline-test'
      }
    }
    stage('Deploy') {
      steps {
        openshiftDeploy 'php-pipeline-test'
      }
    }
    stage('Verify Deployment') {
      steps {
        openshiftVerifyDeployment 'php-pipeline-test'
      }
    }
  }
}