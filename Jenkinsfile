pipeline {
  agent { label "maven" }

  stages {
    stage('maven') {
      steps {
        sh "mvn -version"
        sh "java -version"
      }
    }
  }
}
