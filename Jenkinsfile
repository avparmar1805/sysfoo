pipeline{
	
 agent any

 tools {
     maven 'Maven 3.6.3'
 }

stages {
  stage('one'){
    steps{
	sh 'mvn compile'	
	}
   }
stage('three'){
    steps{
	echo 'package maven app'	
	sh 'mvn package -DskipTests'	
        }
   }
 }
}
