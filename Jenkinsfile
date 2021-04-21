pipeline {
  agent any
  stages {
    stage('build ') {
      steps {
        sh 'mvn install'
      }
    }

    stage('test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('deploy') {
      steps {
        sh 'java -jar target/*.jar'
      }
    }

  }
}