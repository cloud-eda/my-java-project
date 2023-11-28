pipeline {
    agent any

    tools {
        maven 'maven' // 'Maven3' should match the Maven tool name configured in Jenkins
    }
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Run') {
            steps {
                script {
                    sh 'mvn clean install'
                    sh 'java -cp target/my-java-project-1.0-SNAPSHOT.jar com.example.App'
                }
            }
        }
    }
}
