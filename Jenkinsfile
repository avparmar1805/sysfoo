pipeline{
	
 agent any

 tools {
     maven 'Maven 3.6.3'
 }

stages {
  stage('one'){
    steps{
	mvn complie	
	}
   }
stage('two'){
    steps{
	mvn clean test
        }
   }
stage('three'){
    steps{
	mvn package -DskipTests	
        }
   }
 }
}
