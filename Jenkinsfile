pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
               // sh 'mvn clean package -Dmaven.test.failure.ignore=true'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
                //sh 'mvn test -Dmaven.test.failure.ignore=true'
            }
        }
        
        stage('Publishing Junit Tests report ') {
            steps {
                junit 'target/surefire-reports/*.xml'
            }   
        }
        stage('Publishing Code Covergae') {
            steps {
                jacoco()
            }   
        }
       // stage('Deploy') {
       //     steps {
       //         sh 'mvn deploy'
       //     }
       // }
    }
}
