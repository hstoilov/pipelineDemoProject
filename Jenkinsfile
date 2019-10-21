pipeline { 
	agent any 
	tools {
		maven 'Maven 3.6' 
		jdk 'JDK11' 
	}
	stages {
		stage('Compile') {
                 steps {
                    sh mvn compile
                 }
		}
		stage('UnitTest') {
                 steps {
					sh 'mvn resources:testResources'
					sh 'mvn compiler:testCompile'
					sh 'mvn surefire:test'
                 }
		}
	}
}