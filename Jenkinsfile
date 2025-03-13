pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/94sDaniel/hellow-world-jenkins-java.git'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Run') {
            steps {
                sh 'mvn exec:java -Dexec.mainClass="dani.testing.App"'
            }
        }
    }
}