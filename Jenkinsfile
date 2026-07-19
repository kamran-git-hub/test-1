pipeline {
    agent any
    
    tools {
        maven 'Maven-1' 
    }

    stages {
        stage('Clone Java Project') {
            steps {
                echo 'Code clone ho raha hai...'
                git url: 'https://github.com/jglick/simple-maven-project-with-tests.git', branch: 'master'
            }
        }
        stage('Build with Maven') {
            steps {
                echo 'Code build ho raha hai...'
                sh 'mvn clean package' 
            }
        }
        stage('Deploy with Ansible') {
            steps {
                echo 'Ansible Playbook ke zariye code deploy ho raha hai...'
                // Yeh command Jenkins agent par Ansible chalayegi
                sh 'ansible-playbook /home/vboxuser/deploy.yaml' 
            }
        }
    }
}
