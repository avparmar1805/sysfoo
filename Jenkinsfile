pipeline {
  agent {
    docker {
      image 'maven:3.6.3-jdk-11-slim'
    }

  }
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
        archiveArtifacts 'target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}