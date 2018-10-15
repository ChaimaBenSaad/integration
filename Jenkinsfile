pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            build(job: 'test', wait: true, propagate: true)
          }
        }
        stage('First Stage') {
          steps {
            sh '''
#!/bin/sh
echo "Hello world"'''
          }
        }
      }
    }
  }
}