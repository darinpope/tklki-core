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
    stage('test header') {
      parallel {
        stage('test') {
          steps {
            echo 'test1'
          }
        }
        stage('test2') {
          steps {
            echo 'test2'
          }
        }
      }
    }
    stage('integration') {
      steps {
        echo 'integration'
      }
    }
    stage('deploy') {
      parallel {
        stage('dr') {
          steps {
            echo 'dr'
          }
        }
        stage('prod') {
          steps {
            echo 'prod'
          }
        }
      }
    }
  }
}