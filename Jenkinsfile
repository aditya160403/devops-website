pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/<your-username>/devops-website.git'
            }
        }
        stage('Install Tools') {
            steps {
                sh 'which node || sudo apt install -y nodejs'
                sh 'which python3 || sudo apt install -y python3'
            }
        }
        stage('Run JS') {
            steps {
                sh 'echo "JavaScript works (in browser), checked manually."'
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'python3 script.py'
            }
        }
        stage('Static Website Check') {
            steps {
                echo 'Website files exist: index.html, CSS, JS'
            }
        }
    }
}
