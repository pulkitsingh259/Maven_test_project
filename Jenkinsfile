pipeline {
    agent any 
    stages {
        stage('Compile and clean') { 
            steps {
                sh "mvn clean compile"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f /home/jenkins/workspace/JavaPipeline/pom.xml" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f /home/jenkins/workspace/JavaPipeline/pom.xml" 
            }
        }
    }
}

