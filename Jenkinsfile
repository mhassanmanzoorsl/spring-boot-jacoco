pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -Dmaven.test.failure.ignore=true'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -Dmaven.test.failure.ignore=true'
            }
        }
       // stage('Deploy') {
       //     steps {
       //         sh 'mvn deploy'
       //     }
       // }
    }
}
