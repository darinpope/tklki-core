pipeline {
  agent { label 'local-agent' }
  stages {
    stage('build') {
      steps {
        withMaven(maven: 'M3') {
          sh "mvn clean install"
        }
      }
    }
  }
}
