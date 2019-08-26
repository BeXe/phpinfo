pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        openshiftBuild 'php-info-pipeline-test'
      }
    }
    stage('Verify build') {
      steps {
        openshiftVerifyBuild 'php-info-pipeline-test'
      }
    }
    stage('Deploy') {
      steps {
        openshiftDeploy 'php-info-pipeline-test'
      }
    }
    stage('Verify Deployment') {
      steps {
        openshiftVerifyDeployment 'php-info-pipeline-test'
      }
    }
  }
}
