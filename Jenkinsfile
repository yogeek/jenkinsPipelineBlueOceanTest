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
        stage('') {
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
    stage('Front-end') {
      agent {
        docker {
          image 'node:7-alpine'
        }
        
      }
      steps {
        sh 'echo NODE VERSION...'
        sh 'node --version'
      }
    }
  }
}