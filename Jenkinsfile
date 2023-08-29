pipeline {
    agent any 
    tools {
         maven 'maven'
         jdk 'java'
    }
    stages {
        stage('Stage : code scaning') { 
            steps {
                sh 'mvn sonar:sonar'
            }
        }

    stages {
        stage('Stage : Clean') { 
            steps {
                sh 'mvn clean'
            }
        }
         stage('Stage : Validate') { 
            steps {
                sh 'mvn validate'
            }
        }
         stage('Stage : Compile') { 
            steps {
                sh 'mvn compile'
            }
        }
         stage('Stage : Test') { 
            steps {
                sh 'mvn test'
            }
        }
          stage('Stage : Package') { 
            steps {
                sh 'mvn package'
            }
        }
          stage('Stage : Verify') { 
            steps {
                sh 'mvn verify'
            }
        }
          stage('Stage : install') { 
            steps {
                sh 'mvn install'
            }
        }
    }
}
