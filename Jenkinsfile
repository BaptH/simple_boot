pipeline {
    agent any
    
    tools {
        maven 'M3'
    }
    
    stages {
        stage ('Checkout') {
            steps {
                sh 'echo "--=-- Checkout stage --=--"'
                git url:'https://github.com/BaptH/simple_boot.git'
            }
        }
        stage ('Compile') {
            steps {
                sh 'echo "--=-- Compile stage --=--"'
                sh 'mvn clean compile'
            }
        }
        stage ('Test') {
            steps {
                sh 'echo "--=-- Test unitaire --=--"'
                sh 'mvn test'
            }
        }
        stage ('Package') {
            steps {
                sh 'echo "--=-- Package stage --=--"'
                sh 'mvn package'
            }
        }
    }
}