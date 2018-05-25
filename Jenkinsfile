pipeline {
  agent { label 'local-agent' }
  triggers {
    snapshotDependencies()
  }
  stages {
    stage('build') {
      steps {
        withMaven(maven: 'M3') {
          sh "mvn clean deploy"
        }
      }
    }
  }
}
