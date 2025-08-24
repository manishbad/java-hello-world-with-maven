pipeline {
    agent {
        label 'slave1'
    }
    tools {
        maven 'mvn397'    
    }
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/manishbad/java-hello-world-with-maven.git'
            }
        }
        
        stage('Clean') {
            steps {
                sh 'mvn clean'
            }
        }
        
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
         stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                sh 'mvn package'
                sh 'java -jar target/jb-hello-world-maven-0.2.0.jar'
            }
        }
        
    }
}
