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
        sh ' mvn sonar:sonar   -Dsonar.projectKey=org.springframework.samples:spring-petclinic   -Dsonar.host.url=http://127.0.0.1:9000   -Dsonar.login=8566cffba765c59609f95fec076f04113338d8b3'
      }
    }

    stage('deploy') {
      steps {
        sh 'java -jar target/*.jar'
      }
    }

  }
}