pipeline {
  agent {
    docker { 
    label 'docker-slave'
    image 'maven:3.9.3-eclipse-temurin-17' 
    }
    } 
    stages {
    stage('maven') {
      steps {
        sh "mvn -version"
        sh "java -version"
      }
    }
  }
}
