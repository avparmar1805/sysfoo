pipeline {
  agent any
  stages {
    stage('one') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('two') {
      steps {
        sh 'mvn clean test'
      }
    }

    stage('three') {
      steps {
        echo 'package maven app'
        sh 'mvn package -DskipTests'
        archiveArtifacts '/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}