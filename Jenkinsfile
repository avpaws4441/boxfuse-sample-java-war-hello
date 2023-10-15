pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {	
	            	sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/avpaws4441/boxfuse-sample-java-war-hello.git'
            }
        }
	stage('Build') {
            steps {		
                sh 'mvn clean package'
            }
        } 
	stage('Deploy') {
            steps {		
                sh 'sudo cp $WORKSPACE/target/boxfuse-sample-java-war-hello/ /opt/apache-tomcat-10.1.13/webapps'
            }
        }
	    
    }
}
