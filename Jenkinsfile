pipeline {
  agent any
  stages {
    // stage('Clone repository') {
    //   steps {
    //     checkout([$class:'GitSCM',
    //     branches: [[name: '*/main']],
    //     userRemoteConfigs :[[url:'https://github.com/KushShriv/PES2UG21CS053_Jenkins.git']]])
    //   }
    // }
  stage('Build') {
    steps {
      build 'PES2UG21CS053-1'
      sh 'g++ main.cpp -o output'
    }
  }
  stage('Test') {
    steps {
      sh './output'
    }
  }
  stage('Deploy') {
    steps {
      echo 'deploy'
    }
  }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
