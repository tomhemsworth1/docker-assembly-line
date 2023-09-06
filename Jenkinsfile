pipeline {
  agent  { label 'maven' }

  stages {

    stage('maven') {
      agent { label "maven" }
      steps {
        sh "mvn -version"
        sh "java -version"
      }
    }

    stage('node') {
      agent { docker {
        label 'docker-slave'
        image 'node'
      } }
      steps {
        sh "node --version"
      }
    }

    stage('python') {
      agent { docker {
        label 'docker-slave'
        image 'python'
      } }
      steps {
        sh "python3 --version"
      }
    }

    stage('golang') {
      agent { docker {
        label 'docker-slave'
        image 'golang'
      } }
      steps {
        sh "go version"
      }
    }

    stage('gradle') {
      agent { docker {
        label 'docker-slave'
        image 'gradle'
      } }
      steps {
        sh "gradle --version"
      }
    }

  }
}
