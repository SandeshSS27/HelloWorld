pipeline {
    agent any

    tools {
        nodejs 'node'  // This 'node' should match the name in Jenkins Global Tool Config
    }

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/SandeshSS27/HelloWorld.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}

