pipeline {
  agent none
  stages {
    stage('Back-end') {
      parallel {
        stage('Back-end') {
          agent {
            docker {
              image 'maven:3-alpine'
            }
            
          }
          steps {
            sh 'echo MAVEN VERSION...'
            sh 'mvn --version'
          }
        }
        stage('Front-end-parallel') {
          agent {
            docker {
              image 'node:7-alpine'
            }
            
          }
          steps {
            sh 'node --version'
          }
        }
      }
    }
    stage('Last-end') {
      agent {
        docker {
          image 'python'
        }
        
      }
      steps {
        sh 'echo PYTHON VERSION...'
        sh 'python -V'
      }
    }
  }
}