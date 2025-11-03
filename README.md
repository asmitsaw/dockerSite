https://github.com/anliksim/maven-template-bom.git




















pipeline {
    agent any
    stages {
        stage('clone') {
            steps {
                git 'https://github.com/asmitsaw/dockerSite.git'
            }}
            stage('Build') {
            steps {
                bat 'javac hello.java'
            }
            
            }
            stage('run') {
            steps {
                bat 'java hello'
            }
    }
        
    }
}
