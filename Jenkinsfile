pipeline {
  agent any
  stages {
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            echo 'I will compile for the code'
            git(url: 'https://github.com/aespinosa/docker-jenkins', branch: 'master')
          }
        }
        stage('codecheck') {
          steps {
            isUnix()
          }
        }
      }
    }
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh '!/bin/bash'
          }
        }
        stage('build docker') {
          steps {
            sh '!/bin/bash'
          }
        }
      }
    }
    stage('push') {
      steps {
        sh '!/bin/bash'
      }
    }
  }
}