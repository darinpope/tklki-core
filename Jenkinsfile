pipeline {
  agent {
    label 'local-agent'
  }
  stages {
    stage('build') {
      steps {
        sh 'echo hello'
        withMaven(maven: 'M3') {
          sh 'mvn clean install'
        }

      }
    }
  }
}